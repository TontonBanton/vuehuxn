<template>
  <h2>1.Parent Component</h2>
  <ChildCom/>
</template>

<script>
import ChildCom from './1ParentChild.vue'
export default{
  name: 'ParentCom',
  components: {
    ChildCom
  }
}
</script>

<style scoped>
</style>