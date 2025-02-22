<script setup>
const { label, value } = defineProps({
  label: {
    type: String,
    required: true,
  },

  // value range = between 0-10
  value: {
    type: Number,
    default: 0,
    validator: (v) => v >= 0 && v <= 10,
  },
});
</script>

<template>
  <div>
    <h1>{{ label }}</h1>
    <div
      class="h-3 overflow-hidden rounded-full bg-green-900 text-yellow-600 outline"
    >
      <div :class="`h-3 w-${value}/10 rounded-full bg-yellow-500`"></div>
    </div>
  </div>
</template>
