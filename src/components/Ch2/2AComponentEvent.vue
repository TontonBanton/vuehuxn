<template>
  <h2>2. Event $emit() - Child->Parent </h2>

  <h2>Parent Count: {{ count }}</h2>
  <ChildComponent
    @incrementCounter="count++"
    @userInfo="formHandler"
  />
</template>

<script setup>
import { ref } from 'vue'
import ChildComponent from './2BChildComponent';

const count = ref(0)
const formHandler = (username, email, password) => {
  alert(username + email + password) //test
}
</script>

<style scoped>
</style>