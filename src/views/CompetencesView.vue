<template>
  <main class="CompetencesView">
    <MenuTitle :title="title" />
    <TextImageDisplay />
    <DownChevronButton :to="buttonRoute" class="CompetencesView__Chevron" />
  </main>
</template>

<script setup>
import MenuTitle from '@/components/MenuTitle/MenuTitle.vue';
import TextImageDisplay from '@/components/TextImageDisplay/TextImageDisplay.vue'
import DownChevronButton from '@/components/DownChevronButton/DownChevronButton.vue'

const title = "Compétences"
const buttonRoute = "/professional"

</script>

<style scoped>
.CompetencesView {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.CompetencesView__Chevron {
  margin: auto auto 5rem;
}
</style>