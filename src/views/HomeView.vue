<template>
  <main class="HomeView">
    <AppHero />
    <StringBorder :is-title="isTitle" :content="stringBorderContent" />
    <ChevronIcon class="HomeView--Chevron" />
  </main>
</template>

<script setup>
import AppHero from '../components/AppHero/AppHero.vue'
import StringBorder from '../components/StringBorder/StringBorder.vue'
import ChevronIcon from '../components/ChevronIcon/ChevronIcon.vue'

const stringBorderContent = "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus id massa scelerisque, tincidunt nulla quis, malesuada ex.";
const isTitle = false
</script>

<style scoped>
.HomeView {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.HomeView--Chevron {
  margin: auto auto 5rem;
}
</style>