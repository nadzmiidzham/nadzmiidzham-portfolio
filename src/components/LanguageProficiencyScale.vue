<script setup>
const { value } = defineProps({
  // value range
  value: {
    type: Number,
    default: 0,
    validator: (v) => v >= 0 && v <= 10,
  },
});
</script>

<template>
  <div class="my-3">
    <div class="mx-7 my-1 flex gap-1">
      <slot name="icon"></slot>
      <slot class="grow" name="label"></slot>
    </div>

    <div
      class="relative h-3 flex-1 overflow-hidden rounded-full bg-green-900 outline"
    >
      <div
        class="h-full bg-yellow-500"
        :style="{ width: `${(value / 10) * 100}%` }"
      ></div>

      <div
        v-for="level in 10"
        :key="level"
        class="absolute top-0 bottom-0 w-[2px] bg-yellow-200 opacity-50"
        :style="{ left: `${(level / 10) * 100}%` }"
      ></div>
    </div>

    <div class="mt-1 flex justify-between text-green-950">
      <span class="bold">LEARNING</span>
      <span class="bold">PROFICIENT</span>
      <span class="bold">NATIVE</span>
    </div>
  </div>
</template>
