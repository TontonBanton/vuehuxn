<template>
  <h2>Complex Props</h2>
  <h3>{{  users }}</h3>
  <h3>{{ userInfo }}</h3>

  <ul v-for="(name, i) in users" :key="i" >
    <li>{{ name }}</li>
  </ul>
</template>

<script setup>
import { defineProps } from 'vue'
defineProps({
  users: Array,
  userInfo: Object
})
</script>

<style scoped>
li{
  font-size: .8rem;
  text-align: left;
}
</style>
