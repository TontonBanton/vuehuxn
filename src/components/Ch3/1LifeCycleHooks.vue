<template>
  <h2>1. LifeCycle Hooks</h2>
  <div class="row">
    <h3>{{ message }}</h3>
    <button @click="updateMessage">Update the message</button>
  </div>
</template>

<script setup>
import {
  ref,
  onBeforeMount,onMounted,
  onBeforeUpdate,onUpdated,
  onBeforeUnmount,onUnmounted,
} from 'vue'
const message = ref('Default Element')

  onBeforeMount(() => {
    alert('Hook: Component is about to be mounted')
  })
  onMounted(() => {
    alert('Hook: Component has been mounted')
  })
  onBeforeUpdate(() => {
    alert('Hook: Component is about to be updated')
  })
  onUpdated(() => {
    alert('Hook: Component has been updated')
  })
  onBeforeUnmount(() => {
    alert('Hook: Component is about to be unmount')
  })
  onUnmounted(() => {
    alert('Hook: omponent has been unmounted')
  })

  const updateMessage = ()=> {
    message.value = 'Update this element'
  }


</script>

<style scoped>
</style>
