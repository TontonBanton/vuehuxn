<template>
  <h2>Static Props Child</h2>
  <h3>{{ props }}</h3>
  <h3>{{ props.parentName }}</h3>
</template>

<script setup>
import { defineProps } from 'vue';
const props = defineProps(['parentName'])
</script>

<style scoped>
</style>