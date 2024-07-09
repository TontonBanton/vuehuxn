<template>
  <h2>2. Watchers </h2>
  <div class="row">
    <h3>Input Text: {{ message }}</h3>
    <input type="text" v-model="inputTxt" style="width: 9rem;">
  </div>
  <div class="row">
    <h3>Object userName: {{ state.userName }}</h3>
    <button @click="state.userName = 'User2'">Change Object Name</button>
  </div>

  <h3>Default: {{ defaultTxt }}</h3>
  <h3>Counter   : {{ counter }}</h3>
  <div class="row">
    <button @click="defaultTxt='Test'">Change Default</button>
    <button @click="counter++">Increment</button>
  </div>

</template>

<script setup>
import { ref, reactive, watch } from 'vue'
const message = ref('')
const inputTxt = ref('')
const state = reactive({ userName: 'User1' })   //Object
const defaultTxt = ref('Default')
const counter = ref('0')


//Watcher Ref (Basic data)
watch(inputTxt, (newValue, oldvalue) =>{
  console.log("Old: " + oldvalue)
  console.log("New: " + newValue)
  message.value = newValue
})

//Watcher Object (Reactive)
watch(
  () => state.userName, //Getter Function
  (newValue, oldvalue) =>{
    console.log("Old: ", oldvalue)
    console.log("New: ", newValue)
  }
)

//Watcher Multiple Data (Reactive)
watch([defaultTxt, counter], (newValue, oldvalue) =>{
  console.log("Old: " + oldvalue)
  console.log("New: " + newValue)
})

</script>

<style scoped>
</style>