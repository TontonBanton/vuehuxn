<template>
  <h2 class="">5. Global Component</h2>
  <h3 class="globaled">For Global</h3>
  <h3 class="scoped">For Scope</h3>
  <h3 :class="$style['kebab-style']">Using Style Module w/ kebab-case syntax</h3>
  <h3 :class="$style.camelCaseStyle">Using Style Module w/ camelCase syntax</h3>
</template>

<script>
export default{
  name: 'GlobalCom'
}
</script>


<style>
h2 {
  margin: 0;
  text-align: left;
}
h3, p{
  margin: 0;
  padding-left: 20px;
  text-align: left;
}
p {
  color: rgb(140, 168, 16);
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