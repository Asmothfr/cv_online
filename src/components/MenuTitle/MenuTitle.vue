<template>
  <nav :class="{ 'MenuTitle--isOpen': showMenu }">
    <div class="MenuTitle">
      <div class="MenuTitle__titleSection">
        <p>{{ title }}</p>
        <font-awesome-icon @click="switchMenuValue" class="MenuTitle__chevron" :icon="['fas', 'chevron-down']" />
      </div>
      <ul class="MenuTitle__menu">
        <li v-for="filteredInfo in filteredInfos" v-bind:key="filteredInfo">
          <RouterLink class="MenuTitle__link" :to=filteredInfo.route>{{ filteredInfo.pageTitle }}</RouterLink>
        </li>
      </ul>
    </div>
  </nav>
</template>
  
<script setup>
import { ref } from 'vue';
import { RouterLink } from 'vue-router';
import { useRoute } from 'vue-router';

defineProps({
  title: {
    type: String,
    required: true,
  }
})

const route = useRoute()
console.log(route)
const currentRoute = route.fullPath

const routeInfo = [{
  route: "/",
  pageTitle: "Accueil"
},
{
  route: "/competences",
  pageTitle: "Compétences"
},
{
  route: "/professional",
  pageTitle: "Parcours Professionnel"
},
{
  route: "/formations",
  pageTitle: "Formations"
},
]
const filteredInfos = routeInfo.filter((route) => route.route !== currentRoute)

const showMenu = ref(false)
const switchMenuValue = () => {
  showMenu.value = !showMenu.value
}

</script>
  
<style scoped>
@import url(MenuTitle.css);
</style>