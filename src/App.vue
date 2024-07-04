<template>
  <ParentComp/>
  <InterComp/>
  <AttributeComp/>
  <DynamicComp/>
  <EventsComp/>
  <ReactiveComp/>
  <RefComp/>
  <ComputedComp/>
</template>

<script>
import ParentComp from './components/1Parent'
import InterComp from './components/2Interpolation'
import AttributeComp from './components/3AttributeBind'
import DynamicComp from './components/4DynamicBind'
import EventsComp from './components/6Events'
import ReactiveComp from './components/7Reactivity'
import RefComp from './components/8Ref'
import ComputedComp from './components/9Computed'

export default {
  name: 'App',

  components: {
    ParentComp,InterComp, AttributeComp, DynamicComp, EventsComp, ReactiveComp, RefComp, ComputedComp
  }
}
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
