<template>
  <h2>5. Composable (Global Logic JS Function)</h2>
  <h2>Count: {{ counter.count }}</h2>
  <div class="row">
    <button @click="counter.increment">Increment</button>
    <button @click="counter.decrement">Decrement</button>
  </div>
  <h3 style="font-style: italic;">JS Composable Counter Logic Located on Shared Folder</h3>
</template>

<script setup>
import { useCounter } from '../../shared/useCounter'
const counter = useCounter()
</script>

<style scoped>
</style>