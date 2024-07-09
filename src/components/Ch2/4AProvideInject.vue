<template>
  <h2>4. Provide-Inject (Multiple level data passing)</h2>
  <Level1Child/>
  <Level2Child/>
</template>

<script setup>
import { provide } from 'vue'
import Level1Child from './4BInjectChild1'
import Level2Child from './4BInjectChild2'

provide('userName', 'User1')
provide('userAge', 69)
provide('userLocation', ['Ulas', 'Pangi'])

// Using Provide With Array
provide('provideArray', ['User1', 'User2', 'User3'])

// Using Provide With Object
provide('provideObject', {
  id: 1,
  title: 'Epic Adventure Game',
  genre: ['Action', 'Adventure', 'RPG'],
  platform: ['PC', 'PlayStation', 'Xbox', 'Nintendo Switch'],
  releaseDate: '2022-03-15',
  developer: {
    name: 'Awesome Game Studios',
    location: 'San Francisco, CA',
    teamSize: 50
  }
})

// Using Provide With Array Of Objects
provide('provideArrayObject', [
  {
    title: 'Space Explorer',
    genre: 'Sci-Fi',
    platform: 'PC',
    releaseDate: '2023-05-20'
  },
  {
    title: 'Fantasy Quest',
    genre: 'Fantasy',
    platform: 'PlayStation',
    releaseDate: '2023-07-10'
  },
  {
    title: 'Inception',
    director: 'Christopher Nolan',
    genre: 'Sci-Fi',
    releaseDate: '2010-07-16'
  },
  {
    title: 'The Shawshank Redemption',
    director: 'Frank Darabont',
    genre: 'Drama',
    releaseDate: '1994-09-23'
  }
]

)


</script>

<style scoped>
</style>
