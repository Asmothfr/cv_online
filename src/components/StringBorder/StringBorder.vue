<template>
  <div class="StringBorder" :class="{ 'StringBorder--title': isTitle }">
    <p>{{ content }}</p>
  </div>
</template>

<script setup>
defineProps({
  content: {
    type: String,
    required: true,
  },
  isTitle: Boolean
})
</script>

<style>
@import url(StringBorder.css);
</style>