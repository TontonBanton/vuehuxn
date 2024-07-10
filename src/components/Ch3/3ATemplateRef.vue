<template>
  <h2>Template Ref (Direct Reference on DOM)</h2>
  <input type="text" ref="myRef" class="row">
  <h3 :ref="myRefFunc">Header Default Text</h3>

  <ChildComp ref="myCompRef"/>
</template>

<script setup>
import { ref, onMounted } from 'vue';

const myRef = ref('Default')
console.log('Before Mount: ', myRef.value)
onMounted(() =>{
  console.log('On mounted: ', myRef.value)
  myRef.value.focus()
  myRef.value.value = 'Sample Text'
})


//Function Ref
const myRefFunc = (domElem) => {
  console.log(domElem.textContent)
  domElem.textContent = 'Text Changed'
  domElem.style.color = 'red'
}

//Component Ref
import ChildComp from './3BChildCompRef'
const myCompRef = ref(null)
onMounted(() =>{
  console.log(myCompRef.value)
})
</script>

<style scoped>

</style>