<template>
  <h2>2. Interpolation <span v-pre>{{  }}</span> </h2>
  <p> myMessage: {{ myMessage }}, myNumber: {{ myNumber }} </p>
  <p> 2 + 2= {{ 2 + 2 }} </p>
  <p> Add(params) from method  {{ add(3,10) }}</p>
</template>

<script setup>
  const myMessage = "Sample"
  const myNumber = 2

  //Tradion function syntax
  function add(x,y) {
      return x + y
  }
</script>

<style scoped>
</style>