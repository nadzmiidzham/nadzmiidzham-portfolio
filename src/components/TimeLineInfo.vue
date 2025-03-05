<script setup>
const { isStartTime } = defineProps({
  isStartTime: {
    type: Boolean,
    default: false
  }
});
</script>

<template>
  <div class="flex flex-col">
    <div class="flex flex-row text-white gap-3">
      <!-- time -->
      <div class="bg-green-900 px-3 py-2 rounded-xl">
        <b>
          <slot name="time" class="uppercase"></slot>
        </b>
      </div>

      <!-- label -->
      <div class="bg-green-900 px-3 py-2 rounded-xl">
        <b>
          <slot name="label" class="uppercase"></slot>
        </b>
      </div>
    </div>

    <div class="flex flex-row">
      <!-- Timeline Trail -->
      <div v-if="!isStartTime" class="mx-5 bg-green-950 w-[2px]"></div>
      <div v-else>
        <!-- starting timeline line trail -->
        <div class="mx-5 bg-green-950 w-[2px] h-10"></div>

        <!-- starting timeline circle trail -->
        <div class="mx-3">
          <div class="relative flex items-center justify-center h-5 w-5">
            <!-- Outer Circle -->
            <div class="absolute h-5 w-5 rounded-full border-4 border-green-900"></div>
            <!-- Inner Circle -->
            <div class="absolute h-3 w-3 rounded-full bg-green-600"></div>
          </div>
        </div>
      </div>

      <!-- Description -->
      <div class="bg-yellow-200 w-full m-2 p-1 rounded-md outline outline-yellow-600">
        <slot name="description"></slot>
      </div>
    </div>
  </div>
</template>
