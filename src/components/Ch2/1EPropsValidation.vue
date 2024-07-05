<template>
  <h2>Prop Validation</h2>
  <h3>{{ props.fullName }}</h3>
  <h3>{{ props.age }}</h3>
</template>

<script setup>
import { defineProps } from 'vue'
const props = defineProps({
  fullName: {
    type: String,
    required: true,
    default:'anonymous'
  },
  age: Number
})

</script>

<style scoped>
</style>
