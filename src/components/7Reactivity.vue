<template>
  <h2>7. Reactivity </h2>
  <div class="row">
    <h3>Count Reactive: {{ reactiveState.count }}</h3>
    <button @click="reactiveState.count++">+</button>
    <button @click="reactiveState.count--">-</button>
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

<script>
import { reactive }  from 'vue'
export default{
  name:'ReactiveComp',
  data() {
    return{
      reactiveState: reactive({ count:0 }),
      initialState: reactive({ val: { count: 0 }, user: ['User1', 'User2']})
    }
  },
  methods: {
    changeUser() {
      this.initialState.user[0] = 'User3'
      this.initialState.user[1] = 'User4'
    },
    addUser() {
      this.initialState.user.push('User5')
    }
  }
}
</script>

<style scoped>
.row {
  margin-left: 20px;
  display: flex;
  align-items: center;          /* Align items vertically in the center */
  justify-content: flex-start;  /* Start from the left */
}
.row h3 {
  padding: 0;
  font-size: 1rem;
  width: 250px;
}
.row button {
  width: 150px;
}
</style>