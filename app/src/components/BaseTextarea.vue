<template>
  <div class="form-control">
    <label class="label" :for="props.id">
      <span class="label-text font-medium">{{ props.label }}</span>
    </label>
    <textarea
      :id="props.id"
      v-model="modelValue"
      class="textarea textarea-bordered w-full"
      v-bind="$attrs"
    ></textarea>
  </div>
</template>

<script setup lang="ts">
defineOptions({
  inheritAttrs: false,
})

const modelValue = defineModel<string>()

const props = defineProps({
  id: {
    type: String,
    required: true,
  },
  label: {
    type: String,
    required: true,
  },
})
</script>
