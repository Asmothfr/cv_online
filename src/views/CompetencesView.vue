<template>
  <main class="CompetenceView">
    <StringBorder is-title :content="stringBorderContent" />
    <TextImageDisplay />
    <ChevronIcon class="CompetenceView__Chevron" />
  </main>
</template>

<script setup>
import StringBorder from '@/components/StringBorder/StringBorder.vue'
import TextImageDisplay from '@/components/TextImageDisplay/TextImageDisplay.vue'
import ChevronIcon from '@/components/ChevronIcon/ChevronIcon.vue'

const stringBorderContent = "Compétences"
</script>

<style scoped>
.CompetenceView {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.CompetenceView__Chevron {
  margin: auto auto 5rem;
}
</style>