<template>
  <main class="ViewDisplay">
    <AppHero />
    <PresentationCard :content="stringBorderContent" />
    <DownChevronButton :to="route" route class="ChevronView" />
  </main>
</template>

<script setup>
import AppHero from '@/components/AppHero/AppHero.vue'
import PresentationCard from '@/components/PresentationCard/PresentationCard.vue'
import DownChevronButton from '@/components/DownChevronButton/DownChevronButton.vue'

const route = "/competences"
const stringBorderContent = "À la recherche de mon premier emploi en tant que développeur web junior, je suis motivé et prêt à m'impliquer activement au sein d'une équipe.";
</script>

<style scoped></style>