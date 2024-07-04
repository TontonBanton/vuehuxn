<template>
  <h2>9. Computed State</h2>
  <div class="row">
    <h3>Original: {{ number }}</h3>
    <h3>Times 2: {{ mulNumber }}</h3>
  </div>
  <div class="row">
    <h3>FullName: {{ fullName }}</h3>
  </div>
  <div class="row">
    <h3>Original: {{ counter}}</h3>
    <h3>Squared: {{ squareCounter }}</h3>
    <button @click="incrementCount">Increment</button>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue'
const number = ref(5)
const counter = ref(0)
const firstName = ref('John')
const lastName = ref('Wick')

//EXPLICIT w/ return
const mulNumber = computed(() =>{
  return number.value * 2
})
//IMPLICIT
const fullName = computed(() => firstName.value + ' ' + lastName.value )

const incrementCount = () => {
  counter.value++
}
const squareCounter = computed(() => counter.value * 2 )


</script>

<style scoped>
</style>