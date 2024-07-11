<template>
  <h2>8. Data Fetching</h2>
  <button @click="fetchData" class="row">Fetch Data</button>
  <pre>{{ data }}</pre>
</template>

<script setup>
import { ref } from 'vue'
const data = ref(null)

const fetchData = () => {
  // Fetch GET Request- 200-299 response range is OK
  fetch('https://jsonplaceholder.typicode.com/todos/1')
  .then((response) =>{
    if(!response.ok) {
      throw new Error(`Error Status: ${response.status}`)
    }
    return response.json()
  }).then((responseData) => {
    data.value = responseData
  }).catch((error) => {
    console.log(`Error fetching: ${error}`)
  })
}
</script>

<style>
pre {
  text-align: left; /* Ensure text is left-aligned */
  white-space: pre-wrap; /* Wrap the text inside the pre tag */
  word-wrap: break-word; /* Break long words to prevent overflow */
}
</style>