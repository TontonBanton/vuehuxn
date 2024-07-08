<template>
  <img @click="showChapter = 0" src="./assets/logo.png" alt="" width="100rem"><br>
  <button @click="showChapter = 1">Show Chapter 1</button>
  <button @click="showChapter = 2">Show Chapter 2</button>

  <div v-if="showChapter === 1">
    <ParentComp/>
    <InterComp/>
    <AttributeComp/>
    <DynamicComp/>
    <EventsComp/>
    <ReactiveComp/>
    <RefComp/>
    <ComputedComp/>
    <ConditionComp/>
    <IterateComp/>
    <ConnectComp/>
  </div>
  <div v-if="showChapter === 2">
    <PropParentComp/>
    <ComponentEvent/>
    <SlotComp/>
  </div>

</template>

<script setup>
import { ref } from 'vue'
import ParentComp from './components/Ch1/1Parent'
import InterComp from './components/Ch1/2Interpolation'
import AttributeComp from './components/Ch1/3AttributeBind'
import DynamicComp from './components/Ch1/4DynamicBind'
import EventsComp from './components/Ch1/6Events'
import ReactiveComp from './components/Ch1/7Reactivity'
import RefComp from './components/Ch1/8Ref'
import ComputedComp from './components/Ch1/9Computed'
import ConditionComp from './components/Ch1/10ConditionRender'
import IterateComp from './components/Ch1/11IterateArray'
import ConnectComp from './components/Ch1/12TwoWayBind'
import PropParentComp from './components/Ch2/1APropsParent'
import ComponentEvent from './components/Ch2/2AComponentEvent'
import SlotComp from './components/Ch2/3ASlotComponent'

const showChapter = ref(0) //default value
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
