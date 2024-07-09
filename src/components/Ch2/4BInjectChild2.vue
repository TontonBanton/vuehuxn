<template>
  <h3>Child Component 2nd Level</h3>
  <div class="parentinject">
    <h3>List of Datas From Parent up 2 levels</h3>
    <h3>{{ userName }}</h3>
    <h3>{{ userAge }}</h3>
    <h3>{{ userLocation }}</h3>
  </div>

  <h3>Array</h3>
  <ul v-for="(name, i) in userList" :key="i">
    <li>{{ name }}</li>
  </ul>

  <h3>Object</h3>
  <ul v-for="(game, i) in gameObj" :key="i">
    <li>{{ game }}</li>
  </ul>

  <h3>Object Array</h3>
  <ul v-for="(game, i) in gamesArray" :key="i">
    <li>{{ game }}</li>
  </ul>
  <h3>Destructing Object Array</h3>
  <ul v-for="({title, genre, releaseDate}, i) in gamesArray" :key="i">
    <li>Title: {{ title }}</li>
    <li>Genre: {{ genre }}</li>
    <li>Year: {{ releaseDate }}</li>
  </ul>

</template>

<script setup>
import { inject } from 'vue';

const userName = inject('userName')
const userAge = inject('userAge')
const userLocation = inject('userLocation')

const userList = inject('provideArray')
const gameObj = inject('provideObject')
const gamesArray = inject('provideArrayObject')
</script>

<style scoped>
ul, h3{
  margin: 0px;
}
.parentinject, li{
  margin-left: 40px;
}
li {
  font-size: .8rem;
  text-align: left;
}
</style>
