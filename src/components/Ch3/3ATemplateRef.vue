<template>
  <h2>Template Ref (Direct Reference on DOM)</h2>
  <input type="text" ref="myRef" class="row">
  <h3 :ref="myRefFunc">Header Default Text</h3>

  <ChildComp ref="myCompRef"/>
</template>

<script setup>
import ChildComp from './3BChildCompRef'
import { ref, onMounted } from 'vue';
const myRef = ref('Default')
const myCompRef = ref(null)

console.log('Before Mount: ', myRef.value)
//MOUNTED
onMounted(() =>{
  //Element Ref
  console.log('On mounted: ', myRef.value)
  myRef.value.focus()
  myRef.value.value = 'Sample Text'

  //Component Ref
  console.log(myCompRef.value)
})

//Function Ref
const myRefFunc = (domElem) => {
  console.log(domElem.textContent)
  domElem.textContent = 'Text Changed'
  domElem.style.color = 'red'
}

</script>

<style scoped>

</style>