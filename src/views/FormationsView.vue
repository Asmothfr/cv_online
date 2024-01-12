<template>
  <main class="FormationsView">
    <MenuTitle :title="title" />
    <TextInfoFormat :content-page="contentPage" />
    <DownChevronButton :to="route" class="FormationsView__chevron" />
  </main>
</template>

<script setup>
import MenuTitle from '@/components/MenuTitle/MenuTitle.vue';
import TextInfoFormat from '@/components/TextInfoFormat/TextInfoFormat.vue';
import DownChevronButton from '@/components/DownChevronButton/DownChevronButton.vue';

const title = "Formations"
const route = "/"

const contentPage = [{
  startMonth: "Mars",
  startYear: "2022",
  endMonth: "Juillet",
  endYear: "2022",
  description: "Développeur d'application web",
  companyName: "3W Academy",
  companyLocation: "Distanciel"
},
{
  startMonth: "Octobre",
  startYear: "2016",
  endMonth: "Juin",
  endYear: "2017",
  description: "DAEU A",
  companyName: "Paul Valéry",
  companyLocation: "Montpellier"
},
{
  startMonth: "Aout",
  startYear: "2012",
  endMonth: "Juin",
  endYear: "2014",
  description: "CAP ICC",
  companyName: "AFPI",
  companyLocation: "Thiers"
}]
</script>

<style scoped>
.FormationsView {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.FormationsView__chevron {
  margin: auto auto 5rem;
}
</style>