<script setup>
const { showTimelineTrail } = defineProps({
  showTimelineTrail: {
    type: Boolean,
    default: true
  }
});
</script>

<template>
  <div class="flex flex-col gap-2">
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
      <div v-if="showTimelineTrail" class="mx-5 bg-green-950 w-[3px]"></div>
      <div v-else class="mx-5 w-[3px]"></div>

      <!-- Description -->
      <div class="bg-yellow-200 w-full p-1 rounded-md outline outline-yellow-600">
        <slot name="description"></slot>
      </div>
    </div>
  </div>
</template>
