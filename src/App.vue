<template>
  <ParentComp/>
  <InterComp/>
  <AttributeComp/>
  <DynamicComp/>
</template>

<script>
import ParentComp from './components/1Parent.vue'
import InterComp from './components/2Interpolation.vue'
import AttributeComp from './components/3AttributeBind'
import DynamicComp from './components/4DynamicBind'

export default {
  name: 'App',

  components: {
    ParentComp,InterComp, AttributeComp, DynamicComp
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
