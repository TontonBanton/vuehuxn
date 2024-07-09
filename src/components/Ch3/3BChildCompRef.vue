<template>
  <h3>Component Ref (defineExpose)</h3>
  <h3>Count: {{ count }}</h3>
  <div class="row">
    <button @click="increment">Increment</button>
    <button @click="decrement">Decrement</button>
  </div>
</template>

<script setup>
import { ref, defineExpose } from 'vue'
const count = ref(0)
const increment = () => count.value++
const decrement = () => count.value--

defineExpose({ count, increment, decrement})  //Pass this ref on parent
</script>

<style scoped>
</style>