<template>
  <h2>5. Composable (Global JS Logic Function)</h2>
  <h2>Count: {{ counter.count }}</h2>
  <div class="row">
    <button @click="counter.increment">Increment</button>
    <button @click="counter.decrement">Decrement</button>
  </div>
  <h3 style="font-style: italic;">JS Counter Logic located on Shared Folder</h3>
</template>

<script setup>
import { useCounter } from '../../shared/useCounter' //importing composable
const counter = useCounter()
</script>

<style scoped>
</style>