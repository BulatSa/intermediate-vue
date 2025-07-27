<template>
  <h1>Sandbox page</h1>

  <SlotDemo>
    <template #default="{ count }">
      This is my {{ count }}!
    </template>
    <template #footer>
      <p>This is my footer content</p>
    </template>
  </SlotDemo>
</template>

<script setup lang="ts">
import SlotDemo from '@/components/SlotDemo.vue'

</script>
