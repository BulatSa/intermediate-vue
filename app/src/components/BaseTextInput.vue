<template>
  <div class="form-control">
    <label class="label" :for="id">
      <span class="label-text font-medium">{{ props.label }}</span>
    </label>
    <input
      :id="id"
      v-model="firstName"
      class="input input-bordered w-full"
      type="text"
      v-bind="$attrs"
    />
    <input
      :id="id"
      v-model="lastName"
      class="input input-bordered w-full"
      type="text"
      v-bind="$attrs"
    />
  </div>
</template>

<script setup lang="ts">
defineOptions({
  inheritAttrs: false,
})

const firstName = defineModel<string>('firstName');
const lastName = defineModel<string>('lastName');

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
