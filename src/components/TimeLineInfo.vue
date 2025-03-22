<script setup>
const { isStartTime } = defineProps({
  isStartTime: {
    type: Boolean,
    default: false,
  },
});
</script>

<template>
  <div class="flex flex-col">
    <div class="flex flex-row gap-3 text-white">
      <!-- time -->
      <div class="rounded-xl bg-green-900 px-3 py-2">
        <b>
          <slot name="time" class="uppercase"></slot>
        </b>
      </div>

      <!-- label -->
      <div class="rounded-xl bg-green-900 px-3 py-2">
        <b>
          <slot name="label" class="uppercase"></slot>
        </b>
      </div>
    </div>

    <div class="flex flex-row">
      <!-- Timeline Trail -->
      <div v-if="!isStartTime" class="mx-5 w-[2px] bg-green-950"></div>
      <div v-else>
        <!-- starting timeline line trail -->
        <div class="mx-5 h-10 w-[2px] bg-green-950"></div>

        <!-- starting timeline circle trail -->
        <div class="mx-3">
          <div class="relative flex h-5 w-5 items-center justify-center">
            <!-- Outer Circle -->
            <div
              class="absolute h-5 w-5 rounded-full border-4 border-green-900"
            ></div>
            <!-- Inner Circle -->
            <div class="absolute h-3 w-3 rounded-full bg-green-600"></div>
          </div>
        </div>
      </div>

      <!-- Description -->
      <div
        class="m-2 w-full rounded-md bg-yellow-200 p-3 outline outline-yellow-600"
      >
        <slot name="description"></slot>
      </div>
    </div>
  </div>
</template>
