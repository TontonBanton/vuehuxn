<template>
  <h2>Dynamic Props Parent->Child</h2>
  <h3>{{ props.firstName }}</h3>
  <h3>{{ props.lastName }}</h3>
</template>

<script setup>
import { defineProps } from 'vue'
const props = defineProps(['firstName', 'lastName'])
</script>

<style scoped>
</style>