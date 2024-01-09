<template>
  <ul class="TextImageDisplay">
    <li v-for="imgName in imgNameList" :key="imgName.name">
      <div class="TextImageDisplay--ContentBlock">
        <img class="TextImageDisplay--Img" :src="imgDirectory+imgName+extensionFile" alt="">
        <p>{{ imgName }}</p>
      </div>
    </li>
  </ul>
</template>

<script setup>
const imgDirectory = "/textImageDisplayImg/"
const extensionFile = "_logo.png"
const imgNameList = [
  "HTML5",
  "CSS3",
  "JavaScript",
  "PHP",
  "Sql",
  "Postman",
  "Symfony",
  "Vue"
  ]
</script>

<style scoped>
@import url(TextImageDisplay.css);
</style>