<template>
  <h2>4. Async (Load Component on Demand) - defineAsyncComponent </h2>
  <div v-if="showArray">
    <ShowComp/>
  </div>
  <button @click="toggleArray" class="row">Toggle Array List</button>
</template>

<script setup>
//Asynchronous component import
const ShowComp = defineAsyncComponent(() => import('./4BAsyncComp'))

import { ref, defineAsyncComponent } from 'vue'
let showArray = ref(false)
const toggleArray = () => (showArray.value = !showArray.value)

</script>

<style scoped>
</style>