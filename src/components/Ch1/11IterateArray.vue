<template>
  <h2>11. Iterate Array v-for: in :key</h2>
  <div class="row">
    <h3 v-for="(person, index) in peoples" :key="index" class="name"> {{ person }}</h3>
    <ul v-for="num in 5" :key="num"> {{ num }}</ul>
  </div>
  <h3 v-for="(content, i) in books" :key="i"> {{ content }}</h3>

  <ul v-for="({id, title, author, genre}, i) in books" :key="i">
    <li>{{ id }}</li>
    <li>{{ title }}</li>
    <li>{{ author }}</li>
    <li>{{ genre }}</li>
  </ul>

  <ul v-for="(content, i) in books" :key="i">
    <li>{{ content }}</li>
    <li v-for="(property, i) in content" :key="i">{{ property }}</li>
  </ul>

  <ul v-for="(movieArray, i) in movies" :key="i">
    <li v-for="(movie, i) in movieArray" :key="i">{{ movie }}</li>
  </ul>

  <h3 v-for="(value, keys, index) in games" :key="index">
    {{ index }} - {{ keys }} - {{ value }}
  </h3>
  <hr>
</template>

<script setup>
import { ref } from 'vue'
  let peoples = ref(['Juan', 'Pedro', 'Karlo'])
  const books = ref([
    {
      id: 1,
      title: 'Title1',
      author: 'Author1',
      genre: 'Genre1',
      publicationYear: 2001
    },
    {
      id: 2,
      title: 'Title2',
      author: 'Author2',
      genre: 'Genre2',
      publicationYear: 2002
    }
  ])
  //Nested Array
  const movies = [
  ['Inception', 'The Matrix', 'Interstellar', 'The Dark Knight', 'Fight Club'],
  ['Pulp Fiction', 'Forrest Gump', 'The Shawshank Redemption', 'The Godfather', 'The Godfather: Part II'],
  ['The Lord of the Rings: The Fellowship of the Ring', 'The Lord of the Rings: The Two Towers', 'The Lord of the Rings: The Return of the King', 'Star Wars: Episode IV - A New Hope', 'Star Wars: Episode V - The Empire Strikes Back']
  ];

  const games = ref({
  id: 1,
  title: 'Epic Adventure Game',
  genre: ['Action', 'Adventure', 'RPG'],
  platform: ['PC', 'PlayStation', 'Xbox', 'Nintendo Switch'],
  releaseDate: '2022-03-15',
  developer: {
    name: 'Awesome Game Studios',
    location: 'San Francisco, CA',
    teamSize: 50
  },
  ratings: {
    metacritic: 90,
    user: 4.8
  },
  features: {
    singlePlayer: true,
    multiplayer: true,
    onlineCoop: true,
    splitScreen: false
  },
  systemRequirements: {
    minimum: {
      os: 'Windows 10',
      processor: 'Intel Core i5',
      memory: '8 GB RAM',
      graphics: 'NVIDIA GTX 970',
      storage: '50 GB available space'
    },
    recommended: {
      os: 'Windows 11',
      processor: 'Intel Core i7',
      memory: '16 GB RAM',
      graphics: 'NVIDIA RTX 3080',
      storage: '100 GB available space'
    }
  },
  storyline: 'Embark on a thrilling adventure to save the world from impending doom!',
  characters: ['Hero', 'Sidekick', 'Villain', 'NPCs'],
  achievements: [
    { id: 1, name: 'Master Explorer', description: 'Explore every corner of the game world' },
    { id: 2, name: 'Legendary Warrior', description: 'Complete the game on the hardest difficulty' }
  ]
  })

</script>

<style scoped>
.name {
  width: 3rem;
}
li{
  font-size: .8rem;
  text-align: left;
}
</style>