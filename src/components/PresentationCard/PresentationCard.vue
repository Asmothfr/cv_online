<template>
  <div class="PresentationCard">
    <p>{{ content }}</p>
  </div>
</template>

<script setup>
defineProps({
  content: {
    type: String,
    required: true,
  },
})
</script>

<style>
@import url(PresentationCard.css);
</style>