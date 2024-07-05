<template>
  <h2>12. 2-way Binding v-model:</h2>
  <div class="row">
    <h3>{{ formData.username }}</h3>
    <h3>{{ formData.email }}</h3>
    <h3>{{ formData.password }}</h3>
  </div>
  <form class="row" @submit.prevent>
    <input type="text" placeholder="Enter Name" v-model="formData.username">
    <input type="text" placeholder="Enter Email" v-model="formData.email">
    <input type="text" placeholder="Enter Password" v-model="formData.password">
    <button type="submit">Submit</button>
  </form>
</template>

<script setup>
import { ref } from 'vue'
const formData = ref({
  username: '',
  email: '',
  password: ''
})
</script>

<style scoped>
h3{
  width: 11rem;
}
</style>