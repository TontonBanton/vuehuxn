<template>
  <img @click="showChapter = 0" src="./assets/logo.png" alt="" width="80rem"><br>
  <button @click="showChapter = 1">Show Chapter 1</button>
  <button @click="showChapter = 2">Show Chapter 2</button>
  <button @click="showChapter = 3">Show Chapter 3</button>

  <div v-if="showChapter === 1">
    <ParentComp/><hr>
    <InterComp/><hr>
    <AttributeComp/><hr>
    <DynamicComp/><hr>
    <EventsComp/><hr>
    <ReactiveComp/><hr>
    <RefComp/><hr>
    <ComputedComp/><hr>
    <ConditionComp/><hr>
    <IterateComp/><hr>
    <ConnectComp/><hr>
  </div>
  <div v-if="showChapter === 2">
    <PropParentComp/><hr>
    <ComponentEvent/><hr>
    <SlotComp/><hr>
    <ProvideInjectComp/><hr>
  </div>
  <div v-if="showChapter === 3">
    <LifeCycleComp/><hr>
    <WatchersComp/><hr>
    <TemplateRefComp/><hr>
    <AsyncComp/><hr>
    <ComposableComp/><hr>
    <DirectivesComp/><hr>
    <DynamicMainComp/><hr>
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
import ProvideInjectComp from './components/Ch2/4AProvideInject'
import LifeCycleComp from './components/Ch3/1LifeCycleHooks'
import WatchersComp from './components/Ch3/2Watchers'
import TemplateRefComp from './components/Ch3/3ATemplateRef'
import AsyncComp from './components/Ch3/4AAsyncMain'
import ComposableComp from './components/Ch3/5Composable'
import DirectivesComp from './components/Ch3/6Directives'
import DynamicMainComp from './components/Ch3/7ADynamicComp'

const showChapter = ref(0) //default value
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 10px;
}
</style>

<style scoped>
button {
  margin: 3px;
}
</style>