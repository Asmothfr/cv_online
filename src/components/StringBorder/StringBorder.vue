<template>
  <div class="StringBorder" :class="{ 'StringBorder--Title' : isTitle, 'StringBorder--Text' : !isTitle }">
    <p>{{ content }}</p>
  </div>
</template>

<script setup>
defineProps({
  content: {
    type: String,
    required: true,
  },
  isTitle : {
    type: Boolean,
    required: true
  }
})
</script>

<style>
  @import url(StringBorder.css);
</style>