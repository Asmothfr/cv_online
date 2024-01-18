<template>
  <div>
    <RouterView v-slot="{ Component }">
      <transition name="route" mode="out-in">
        <component :is="Component" />
      </transition>
    </RouterView>
  </div>
</template>

<script setup>
import { RouterView } from 'vue-router'
</script>

<style scoped>
.route-enter-from {
  opacity: 0;
  transform: translateY(200px);
}

.route-enter-active {
  transition: all 0.5s ease-out;
}

.route-leave-to {
  opacity: 0;
  transform: translateY(-200px);
}

.route-leave-active {
  transition: all 0.5s ease-in;
}
</style>
