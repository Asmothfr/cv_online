<template>
  <main class="ProfessionalView">
    <StringBorder is-title :content="StringBorderContent" />
    <TextInfoFormat :content-page="contentPage" />
    <DownChevronButton :route="route" class="ProfessionalView__chevron" />
  </main>
</template>

<script setup>
import StringBorder from '@/components/StringBorder/StringBorder.vue'
import TextInfoFormat from '@/components/TextInfoFormat/TextInfoFormat.vue'
import DownChevronButton from '@/components/DownChevronButton/DownChevronButton.vue'

const route = "/formations"
const StringBorderContent = "Parcour Professionnel"

const contentPage = [{
  startMonth: "Juin",
  startYear: "2023",
  endMonth: "Janvier",
  endYear: "2023",
  description: "Facteur",
  companyName: "La Poste",
  companyLocation: "Laguiole"
},
{
  startMonth: "Mai",
  startYear: "2021",
  endMonth: "Novembre",
  endYear: "2021",
  description: "Coutellier",
  companyName: "La Coutellerie de",
  companyLocation: "Laguiole"
},
{
  startMonth: "Août",
  startYear: "2018",
  endMonth: "Janvier",
  endYear: "2020",
  description: "Manoeuvre Frigoriste",
  companyName: "Frigevar",
  companyLocation: "Nîmes"
},
{
  startMonth: "Novembre",
  startYear: "2017",
  endMonth: "Mars",
  endYear: "2018",
  description: "Conditionneur",
  companyName: "Horiba Médical",
  companyLocation: "Montpellier"
},
{
  startMonth: "Juillet",
  startYear: "2012",
  endMonth: "Septembre",
  endYear: "2015",
  description: "Coutellier",
  companyName: "Le Camarguais",
  companyLocation: "Bezouces"
}
]


</script>

<style scoped>
.ProfessionalView {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.ProfessionalView__chevron {
  margin: auto auto 5rem;
}
</style>