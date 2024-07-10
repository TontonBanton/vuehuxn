<template>
  <h2>3. Slot Components( Parent-Child DOM Elements) v-slot</h2>
  <SlotComp>
    <h3>Header From Parent->Child</h3>
  </SlotComp>

  <FallbackContent></FallbackContent>

  <NamedSlot>
      <template v-slot:one>
        <h3>This header will go to child slot named one </h3>
      </template>
      <template v-slot:two>
        <h3>This header will go to child slot named two </h3>
      </template>
  </NamedSlot>

  <DefaultSlot>
    <template #default>
      <h3>Header from Parent Default Slot </h3>
    </template>
  </DefaultSlot>

</template>


<script setup>
import SlotComp from './3BSlotChild'
import FallbackContent from './3CFallbackContent'
import NamedSlot from './3DNamedSlot'
import DefaultSlot from './3EDefaultSlot'
</script>

<style scoped>
</style>