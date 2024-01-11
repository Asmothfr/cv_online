<template>
  <RouterLink class=" DownChevronButton">
    <font-awesome-icon class="DownChevronButton__style" :icon="['fas', 'chevron-down']" />
  </RouterLink>
</template>

<script setup>
import { RouterLink } from 'vue-router';
</script>

<style>
@import url(DownChevronButton.css);
</style>