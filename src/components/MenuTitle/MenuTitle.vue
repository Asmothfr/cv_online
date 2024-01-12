<template>
  <nav>
    <ul>
      <li class="MenuTitle">
        <p class="MenuTitle__title">{{ title }}</p>
        <ul>
          <li v-for="filteredInfo in filteredInfos" v-bind:key="filteredInfo">
            <RouterLink :to=filteredInfo.route>{{ filteredInfo.pageTitle }}</RouterLink>
          </li>
        </ul>
      </li>
    </ul>
  </nav>
</template>
  
<script setup>
import { RouterLink } from 'vue-router';
import { useRoute } from 'vue-router';

defineProps({
  title: {
    type: String,
    required: true,
  }
})

const route = useRoute()
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
</script>
  
<style scoped>
@import url(MenuTitle.css);
</style>