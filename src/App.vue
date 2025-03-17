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
  <div class="hidden grid-cols-7 justify-items-center gap-4 py-7 md:grid">
    <div class="col-span-1"></div>
    <div class="col-span-3"><DetailSectionLayout /></div>
    <div class="sticky top-7 col-span-2 self-start">
      <SummarySectionLayout />
    </div>
    <div class="col-span-1"></div>
  </div>
</template>
