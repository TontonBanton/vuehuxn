<template>
  <div class="container">
    <button @click="$emit('incrementCounter')">Child Button</button>
  </div>
  <form @submit.prevent="$emit('userInfo', username, email, password )">
    <input type="text" v-model="username" placeholder="name">
    <input type="text" v-model="email" placeholder="email">
    <input type="text" v-model="password" placeholder="password">
    <button type="submit">Submit</button>
  </form>
</template>

<script setup>
import { ref } from 'vue'
const username = ref('')
const email = ref('')
const password = ref(' ')
</script>

<style scoped>
h3 {
  margin: 0px;                  /* h3 already has global margin of 20px*/
}
.container, form {
  margin-left: 20px;
  display: flex;
  align-items: center;          /* Align items vertically in the center */
  justify-content: flex-start;  /* Start from the left */
}
</style>