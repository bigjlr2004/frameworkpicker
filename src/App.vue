<script setup>
import { ref } from 'vue'
const imgSrc = ref('null')
const framework = ref('')

const handleAngular = () => {
  imgSrc.value =
    'https://github.com/nashville-software-school/Vue-Workshop/blob/main/assets/framework-picker-logos/angular_logo.png?raw=true'
  framework.value = 'Angular'
}
const handleReact = () => {
  imgSrc.value =
    'https://github.com/nashville-software-school/Vue-Workshop/blob/main/assets/framework-picker-logos/react_logo.png?raw=true'
  framework.value = 'React'
}
const handleVue = () => {
  imgSrc.value =
    'https://github.com/nashville-software-school/Vue-Workshop/blob/main/assets/framework-picker-logos/vue_logo.png?raw=true'
  framework.value = 'Vue'
}
</script>

<template>
  <div>
    <h1>Hello FrontEnd Developers</h1>
  </div>
  <div>
    <h1>What is your favorite JS Framework?</h1>
  </div>
  <div>
    <button @click="handleAngular">Angular</button>
    <button @click="handleVue">Vue</button>
    <button @click="handleReact">React</button>
  </div>
  <div v-if="framework">
    <p>Good choice! {{ framework }} is a good tool.</p>
  </div>

  <div>
    <img :src="imgSrc" alt="" />
  </div>
</template>

<style scoped></style>
