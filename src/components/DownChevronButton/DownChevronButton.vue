<template>
  <div>
    <button class="DownChevronButton">
      <RouterLink class="DownChevronButton__link" :to="route">
        <font-awesome-icon class="DownChevronButton--Style" :icon="['fas', 'chevron-down']" />
      </RouterLink>
    </button>
  </div>
</template>

<script setup>
import { RouterLink } from 'vue-router';
defineProps({
  route: {
    type: String,
    required: true
  }
})
</script>

<style>
@import url(DownChevronButton.css);
</style>