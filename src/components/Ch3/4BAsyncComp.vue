<template>
  <h3>Async Component Child Render</h3>
  <h3 v-for="(user, i ) in arrayList" :key="i">
    {{ user }}
  </h3>
</template>

<script setup>
import { ref } from 'vue'
const arrayList = ref(['User1', 'User2', 'User3', 'User4',])
</script>

<style scoped>
</style>