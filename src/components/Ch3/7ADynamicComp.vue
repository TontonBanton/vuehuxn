<template>
  <h2>7. Dynamic Rendering Components - component:is</h2>
  <div class="row" style="margin-top: 10px;">
    <button @click="currentTab = 'Component1'">Component 1</button>
    <button @click="currentTab = 'Component2'">Component 2</button>
    <button @click="currentTab = 'Component3'">Component 3</button>
  </div>

  <component :is="tabs[currentTab]" />   <!--Rendering component tabs-->
</template>

<script setup>
import { ref } from 'vue'
import Component1 from './7BComponent1'
import Component2 from './7BComponent2'
import Component3 from './7BComponent3'

const currentTab = ref('Component1')  //default
const tabs = {
  Component1,
  Component2,
  Component3
}
</script>

<style scoped>
</style>