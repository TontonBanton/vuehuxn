<template>
  <h2>7. Reactive State (Object) </h2>
  <div class="row">
    <h3>Count Reactive: {{ reactiveState.count }}</h3>
    <button @click="reactiveState.count++">Increment</button>
    <button @click="reactiveState.count--">Decrement</button>
  </div>
  <div class="row">
    <h3> Current Count: {{ initialState.val.count }}</h3>
    <button @click="initialState.val.count += 10">Add 10</button>
  </div>
  <div class="row">
    <h3> Users: {{ initialState.user }}</h3>
    <button @click="changeUser">Change User Property</button>
    <button @click="addUser">Add User Propert</button>
  </div>
</template>

<script setup>
import { reactive }  from 'vue'

  let reactiveState = reactive({
    count:0
  })
  let initialState = reactive({
    val: { count: 0 },
    user: ['User1', 'User2']
  })

  function changeUser() {
    initialState.user[0] = 'User3'
    initialState.user[1] = 'User4'
  }
  function addUser() {
    initialState.user.push('User5')
  }
</script>

<style scoped>
</style>