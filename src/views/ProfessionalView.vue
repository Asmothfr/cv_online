<template>
  <main class="ProfessionalView">
    <StringBorder :is-title="isTitle" :content="StringBorderContent" />
    <TextInfoFormat :content-page="contentPage"/>
    <ChevronIcon class="ProfessionalView--Chevron" />
  </main>
</template>

<script setup>
import StringBorder from '../components/StringBorder/StringBorder.vue'
import ChevronIcon from '../components/ChevronIcon/ChevronIcon.vue'
import TextInfoFormat from '../components/TextInfoFormat/TextInfoFormat.vue'

const isTitle = true
const StringBorderContent = "Parcour Professionnel"

const contentPage = {
   0:{
    startMonth: "Juin",
    startYear: "2023",
    endMonth: "Janvier",
    endYear: "2023",
    description: "Facteur",
    companyName: "La Poste",
    companyLocation: "Laguiole"
  },
   1:{
    startMonth: "Mai",
    startYear: "2021",
    endMonth: "Novembre",
    endYear: "2021",
    description: "Coutellier",
    companyName: "La Coutellerie de",
    companyLocation: "Laguiole"
  },
   2:{
    startMonth: "Août",
    startYear: "2018",
    endMonth: "Janvier",
    endYear: "2020",
    description: "Manoeuvre Frigoriste",
    companyName: "Frigevar",
    companyLocation: "Nîmes"
  },
   3:{
    startMonth: "Novembre",
    startYear: "2017",
    endMonth: "Mars",
    endYear: "2018",
    description: "Conditionneur",
    companyName: "Horiba Médical",
    companyLocation: "Montpellier"
  },
   4:{
    startMonth: "Juillet",
    startYear: "2012",
    endMonth: "Septembre",
    endYear: "2015",
    description: "Coutellier",
    companyName: "Le Camarguais",
    companyLocation: "Bezouces"
  }
}


</script>

<style scoped>
.ProfessionalView {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.ProfessionalView--Chevron {
  margin: auto auto 5rem;
}
</style>