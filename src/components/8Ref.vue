<template>
  <h2>8. Ref (for primitive value) </h2>
  <div class="row">
    <h3>Number Ref: {{ refNum }}</h3>
    <button @click="refNum++">+</button>
    <button @click="refNum--">-</button>
  </div>
  <div class="row">
    <h3>String Ref: {{ refString }}</h3>
    <button @click="refString = 'User'">Pass String</button>
  </div>
  <div class="row">
    <h3>Array Ref: {{ refArray }}</h3>
    <button @click="refArray.push('User3')">Array Push</button>
  </div>
  <div>
    <h3>Name: {{ userInfo.name }}</h3>
    <h3>Age: {{ userInfo.age }}</h3>
    <h3>Location: {{ userInfo.location }}</h3>
    <h3>isMarried: {{ userInfo.isMarried }}</h3>
  </div>
  <div class="row">
    <button @click="userInfo.name = 'ChangeName'">Change Name</button>
    <button @click="userInfo.age = 18">Change Age</button>
    <button @click="userInfo.location = ['change', 'change']">Change Location</button>
    <button @click="userInfo.isMarried = true">Change Status</button>
  </div>
</template>

<script>
import { ref } from 'vue'
export default{
  name:'RefComp',
  data() {
    return{
      refNum: ref(0),
      refString: ref(''),
      refArray: ref(['User1', 'User2']),
      userInfo:ref({ name:'Juan', age:13, location:['Ulas', 'Pangi'], isMarried: false })
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