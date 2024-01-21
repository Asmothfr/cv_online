<template>
  <div>
    <RouterView v-slot="{ Component, route }">
      <transition :name="route.meta.transition" mode="out-in">
        <component :is="Component" />
      </transition>
    </RouterView>
  </div>
</template>

<script setup>
import { RouterView, useRouter } from 'vue-router'

const router = useRouter();
const routes = router.options.routes

router.afterEach((to, from) => {
  const toRoute = to.path
  const fromRoute = from.path

  const toRouteIndex = routes.findIndex(route => {
    return route.path === toRoute
  })
  const fromRouteIndex = routes.findIndex(route => {
    return route.path === fromRoute
  })

  to.meta.transition = toRouteIndex > fromRouteIndex ? 'routeUp' : 'routeDown'
})
</script>

<style>
@import url(assets/styles/utils.css);

.routeUp-enter-from {
  opacity: 0;
  transform: translateY(100px);
}

.routeUp-leave-to {
  opacity: 0;
  transform: translateY(-100px);
}

.routeUp-enter-active,
.routeUp-leave-active {
  transition: all 0.5s ease-out;
}

.routeDown-enter-from {
  opacity: 0;
  transform: translateY(-100px);
}

.routeDown-leave-to {
  opacity: 0;
  transform: translateY(100px);
}

.routeDown-enter-active,
.routeDown-leave-active {
  transition: all 0.5s ease-out;
}
</style>
