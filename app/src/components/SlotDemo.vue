<template>
  <main>
    <slot name="header">
      <h1>Slot demo header</h1>
    </slot>
    <slot :count="currentCount">
      Current count {{ currentCount }}
    </slot>
    <footer v-if="slots.footer" class="footer-class">
      <slot name="footer" />
    </footer>
  </main>
</template>

<script setup lang="ts">
import {ref, useSlots} from 'vue'

const slots = useSlots()

const currentCount = ref(10)
</script>
