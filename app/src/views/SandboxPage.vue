<template>
  <h1>Sandbox page</h1>

  <SlotDemo>
    <template #default="{ count }">
      This is my {{ count }}!
    </template>

  </SlotDemo>
</template>

<script setup lang="ts">
import SlotDemo from '@/components/SlotDemo.vue'

</script>
