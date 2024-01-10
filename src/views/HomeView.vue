<template>
  <main class="HomeView">
    <AppHero />
    <StringBorder :content="stringBorderContent" />
    <ChevronIcon class="HomeView__chevron" />
  </main>
</template>

<script setup>
import AppHero from '@/components/AppHero/AppHero.vue'
import StringBorder from '@/components/StringBorder/StringBorder.vue'
import ChevronIcon from '@/components/ChevronIcon/ChevronIcon.vue'

const stringBorderContent = "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus id massa scelerisque, tincidunt nulla quis, malesuada ex.";
</script>

<style scoped>
.HomeView {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.HomeView__chevron {
  margin: auto auto 5rem;
}
</style>