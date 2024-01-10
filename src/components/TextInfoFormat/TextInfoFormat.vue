<template>
  <div class="TextInfoFormat">
    <div class="TextInfoFormat__content" v-for="object in contentPage" v-bind:key="object.object">
      <div class="TextInfoFormat__dateBlock">
        <div class="TextInfoFormat__date">
          <p>{{ object.startMonth }}</p>
          <p class="TextInfoFormat__years TextInfoFormat--detailColor">{{ object.startYear }}</p>
        </div>
        <div class="TextInfoFormat__date">
          <p>{{ object.endMonth }}</p>
          <p class="TextInfoFormat__years TextInfoFormat--detailColor">{{ object.endYear }}</p>
        </div>
      </div>
      <div>
        <p>{{ object.description }}</p>
        <div class="TextInfoFormat__company">
          <p class="TextInfoFormat--detailColor">{{ object.companyName }}</p>
          <p class="TextInfoFormat__location"> {{ object.companyLocation }} </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  contentPage: {
    type: Object,
    required: true
  }
})
</script>

<style scoped>
@import url(TextInfoFormat.css);
</style>