<template>
  <h2 class="">5. Global Component</h2>
  <h3 class="globaled">For Global</h3>
  <h3 class="scoped">For Scope</h3>
  <h3 :class="$style['kebab-style']">Using Style Module w/ kebab-case syntax</h3>
  <h3 :class="$style.camelCaseStyle">Using Style Module w/ camelCase syntax</h3>
  <hr>
</template>

<script setup>
</script>

<style>
.row {
  margin-left: 20px;
  display: flex;
  align-items: center;          /* Align items vertically in the center */
  justify-content: flex-start;  /* Start from the left */
}
.row h3 {
  padding: 0;
  width: 250px;
}
.row button {
  width: 150px;
}

h2 {
  font-size: 1rem;
  margin: 0;
  text-align: left;
}
h3, p, a{
  font-size: .8rem;
  margin: 0;
  padding-left: 20px;
  text-align: left;
}
.globaled {
  color: rgb(99, 10, 10);
}
</style>

<style scoped>
  .scoped {
    color: rgb(44, 27, 201);
  }

</style>

<style module>
  .kebab-style {
    color:blueviolet
  }
  .camelCaseStyle {
    color:rgb(243, 63, 63)
  }
</style>