<template>
  <h2>10. Conditioal v-if:</h2>
  <h3 v-if="boolVal">This header will show on True removed on DOM if false</h3>
  <h3 v-else>This will show on False</h3>
  <div class="row">
    <h3 v-show="isVisible">Visible on true only hide if false</h3>
    <button @click="isVisible = !isVisible">Visible value: {{ isVisible }}</button>
  </div>
  <div class="row">
    <h3 v-if="isUserLoggedIn">Welcome, {{ userName }}</h3>
    <h3 v-else>Please Login to access</h3>
    <h3 v-show="showDetails">Show Details</h3>
    <button @click="isUserLoggedIn = !isUserLoggedIn">Log Value: {{ isUserLoggedIn }}</button>
  </div>
  <div class="row" v-if="isActive">
    <p>This whole div will not show if isActive is false</p>
  </div>
  <div class="row">
    <h3 v-if="password.length >= 8 ">Strong Password</h3>
    <h3 v-else-if="password.length < 8">Weak Password</h3>
    <h3 v-else>Please Enter Password</h3>
  </div>
  <hr>
</template>

<script setup>
import { ref } from 'vue'
  const boolVal = true
  const isVisible = ref(true)
  const isActive = ref(true)

  let isUserLoggedIn = ref(true)
  let userName = 'JohnWick'
  let showDetails = ref(isUserLoggedIn)
  let password = ref('12345678')
  //let password = ref('12345')
   //let password = ref(0)
</script>

<style scoped>
</style>