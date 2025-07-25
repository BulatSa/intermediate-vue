<template>
  <h1>helko</h1>
  <p>{{ firstName }} - {{ lastName }}</p>
  <BaseTextInput id="base" placeholder="Hello" label="First Name" v-model:first-name="firstName" v-model:last-name="lastName" />
  <BaseTextarea />
</template>

<script setup lang="ts">
import BaseTextarea from '@/components/BaseTextarea.vue'
import BaseTextInput from '@/components/BaseTextInput.vue'
import { ref } from 'vue'

const firstName = ref('')
const lastName = ref('')
</script>
