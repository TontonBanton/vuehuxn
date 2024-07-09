<template>
  <h2>1. Properties (props) - Parent -> Child</h2>

  <StaticChild parentName="Juan"/>
  <DynamicChild :firstName="firstName" :lastName="lastName"/>
  <ChangingProps :varNum="varNum" />
  <PropsValidation fullName="JohnWick" :age="30"/>

  <ComplexProps
    :users="['User1','User2','User3']"
    :userInfo="{ name: 'Juan Tamad', age: 69, location: ['Boulevard', 'Achup']}"
  />
  <CustomValidation name="User1" :age="45" password="12345"/>

</template>

<script setup>
import { ref } from 'vue'
import StaticChild from './1BStaticChild'
import DynamicChild from './1CDynamicChild'
import ChangingProps from './1DChangingProps'
import PropsValidation from './1EPropsValidation'
import ComplexProps from './1FComplexProps'
import CustomValidation from './1GCustomValidation'

  const firstName = ref('Juan')
  const lastName = ref('Wick')
  const varNum = ref(13)

</script>

<style>
h2, h3 {
  margin-left: 20px;
}
</style>

<style scoped>
h2{
  margin-left: 0px;
}
</style>