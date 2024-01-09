<template>
  <div class="TextInfoFormat">
    <div class="TextInfoFormat--Content"
     v-for="object in contentPage"
    v-bind:key="object.object"
    >
      <div class="TextInfoFormat--DateBlock">
        <div class="TextInfoFormat--Date">
          <p>{{ object.startMonth }}</p>
          <p class="TextInfoFormat--Years TextInfoFormat--DetailColor">{{ object.startYear }}</p>
        </div>
        <div class="TextInfoFormat--Date">
          <p>{{ object.endMonth }}</p>
          <p class="TextInfoFormat--Years TextInfoFormat--DetailColor">{{ object.endYear }}</p>
        </div>
      </div>
      <div>
        <p>{{ object.description }}</p>
        <div class="TextInfoFormat--Company">
          <p class="TextInfoFormat--DetailColor">{{ object.companyName }}</p>
          <p class="TextInfoFormat--Location"> {{ object.companyLocation }} </p>
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