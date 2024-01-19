<template>
  <main class="ViewDisplay">
    <MenuTitle :title="title" />
    <TextImageDisplay />
    <DownChevronButton :to="buttonRoute" class="ChevronView" />
  </main>
</template>

<script setup>
import MenuTitle from '@/components/MenuTitle/MenuTitle.vue';
import TextImageDisplay from '@/components/TextImageDisplay/TextImageDisplay.vue'
import DownChevronButton from '@/components/DownChevronButton/DownChevronButton.vue'

const title = "Compétences"
const buttonRoute = "/professional"

</script>

<style scoped></style>