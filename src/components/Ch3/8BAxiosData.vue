<template>
  <h2>9. AXIOS (install npm axios) </h2>
  <button @click="fetchData" class="row">Fetch Axios </button>
  <pre>{{ data }}</pre>
</template>

<script setup>
import { ref } from 'vue'
import axios from 'axios'
const data = ref(null)

const fetchData = async () => {
  try{
    //AXIOS GET request
    const response = await axios.get('https://jsonplaceholder.typicode.com/todos/1')
    data.value = response.data
  } catch (error) {
    console.log(`Error fetching data: ${error}`)
  }
}
</script>

<style scoped>
</style>