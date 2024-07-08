<template>
  <h2>Complex Props</h2>
  <h3>{{  users }}</h3>
  <h3>{{ userInfo }}</h3>

  <ul v-for="(name, i) in users" :key="i" >
    <li margin="0">{{ name }}</li>
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
ul{
  margin: 0px;
}
li {
  margin: 0px;
  font-size: .8rem;
  text-align: left;
}
</style>