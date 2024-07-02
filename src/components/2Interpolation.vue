<template>
  <h2>2. Interpolation <span v-pre>{{  }}</span> </h2>
  <p> myMessage: {{ myMessage }}, myNumber: {{ myNumber }} </p>
  <p> 2 + 2= {{ 2 + 2 }} </p>
  <p> Add(params) from method  {{ add(3,10) }}</p>
</template>

<script>

export default {
  name: 'InterComp',
  data() {
    return {
      myMessage: "Sample",
      myNumber: 2
    }
  },
  methods: {
    add(x,y) {
      return x + y
    }
  }
}
</script>

<style scoped>
</style>