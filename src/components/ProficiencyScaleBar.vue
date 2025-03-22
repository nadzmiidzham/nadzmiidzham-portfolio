<script setup>
import { computed } from "vue";

const { value } = defineProps({
  // value range
  value: {
    type: Number,
    default: 0,
    validator: (v) => v >= 0 && v <= maxValue,
  },
});

const maxValue = 10;
const barValue = computed(() => {
  return (value / maxValue) * 100;
});
</script>

<template>
  <div class="my-1">
    <div class="my-1 flex gap-1">
      <slot name="icon"></slot>
      <slot class="grow" name="label"></slot>
    </div>
    <div
      class="h-3 overflow-hidden rounded-full bg-green-900 text-yellow-600 outline"
    >
      <div
        :class="`h-3 rounded-full bg-yellow-500`"
        :style="{ width: `${barValue}%` }"
      ></div>
    </div>
  </div>
</template>
