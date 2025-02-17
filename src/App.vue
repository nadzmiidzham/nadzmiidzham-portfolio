<script setup>
import DetailSection from "./sections/DetailSection.vue";
import SummarySection from "./sections/SummarySection.vue";
</script>

<template>
  <div class="grid grid-cols-6 gap-4">
    <div class="col-span-1"></div>
    <div class="col-span-3"><DetailSection /></div>
    <div class="col-span-1"><SummarySection /></div>
    <div class="col-span-1"></div>
  </div>
</template>
