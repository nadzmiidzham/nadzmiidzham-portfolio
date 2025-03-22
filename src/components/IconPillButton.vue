<script setup>
const { label, iconPath, linkUrl } = defineProps({
  label: String,
  iconPath: String,
  linkUrl: {
    type: String,
    default: "#",
  },
});
</script>

<template>
  <a :href="linkUrl" target="_blank">
    <button
      class="rounded-full bg-green-900 px-3 py-1 text-yellow-300 hover:bg-yellow-100 hover:text-green-700"
    >
      <div class="flex flex-row gap-1">
        <img class="my-auto h-5 w-5" :src="iconPath" />
        <span class="font-bold">
          {{ label }}
        </span>
      </div>
    </button>
  </a>
</template>
