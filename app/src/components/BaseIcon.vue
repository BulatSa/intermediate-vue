<template>
  <Icon v-if="source == 'iconify'" :icon="name" :width="width" :height="height" />
  <component v-else :is="customIcon"></component>
</template>

<script setup lang="ts">
import {computed, defineAsyncComponent} from 'vue'
import { Icon } from '@iconify/vue'

const props = defineProps({
  name: {
    type: String,
    required: true
  },
  source: {
    type: String,
    default: 'iconify'
  },
  width: {
    type: Number,
    default: 20
  },
  height: {
    type: Number,
    default: 20
  }
})

const customIcon = computed(() => {
  if (props.name !== 'iconify') {
    return defineAsyncComponent(() => import(`@/components/icons/${props.name}.vue`))
  } else {
    return null;
  }
})

</script>
