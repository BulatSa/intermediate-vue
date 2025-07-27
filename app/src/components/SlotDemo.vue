<template>
  <main>
    <slot name="header">
      <h1>Slot demo header</h1>
    </slot>
    <slot :count="currentCount">
      Current count {{ currentCount }}
    </slot>
    <slot name="footer">
      <p>This is footer</p>
    </slot>
  </main>
</template>

<script setup lang="ts">
import {ref} from 'vue'

const currentCount = ref(10)
</script>
