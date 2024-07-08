<template>
  <h2>Custom Props Validation</h2>
  <h3>{{ name }}</h3>
  <h3>{{ age }}</h3>
  <h3>{{ password }}</h3>
</template>

<script setup>
import { defineProps } from 'vue'
defineProps({
  name:{
    type: String,
    validator: (propValue) => {
      return ['User1', 'User2', 'User3'].includes(propValue)                       //curly braces
    }
  },
  age: {
    type: Number,
    validator: (propValue) => ( propValue >= 18 && propValue <=30 ? true: false )  //parenthesis
  },
  password: {
    type: String,
    validator: (propValue) => propValue >= 8
  }
})
</script>

<style scoped>
</style>