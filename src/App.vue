<script setup>
import DetailSectionLayout from "./layouts/DetailSectionLayout.vue";
import SummarySectionLayout from "./layouts/SummarySectionLayout.vue";
</script>

<template>
  <!-- mobile view -->
  <div class="flex flex-col md:hidden">
    <SummarySectionLayout />
    <DetailSectionLayout />
  </div>

  <!-- desktop view -->
  <div class="mx-7 hidden flex-row justify-items-center md:flex">
    <div class="grow">
      <DetailSectionLayout />
    </div>
    <div class="sticky top-7 self-start">
      <SummarySectionLayout />
    </div>
  </div>
</template>
