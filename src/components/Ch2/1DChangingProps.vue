<template>
  <h2>Changing Props Not Allowed (read-only)</h2>
  <h3>{{ props.varNum }}</h3>
</template>

<script setup>
import { defineProps } from 'vue'
const props = defineProps(['varNum'])
</script>

<style scoped>
</style>
