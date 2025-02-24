<script setup>
import DetailSectionLayout from "./layouts/DetailSectionLayout.vue";
import SummarySectionLayout from "./layouts/SummarySectionLayout.vue";
</script>

<template>
  <div class="flex flex-col gap-10">
    <SummarySectionLayout />
    <DetailSectionLayout />
  </div>
  <!-- <div class="grid grid-cols-6 justify-items-center gap-4 py-7">
    <div class="col-span-1"></div>
    <div class="col-span-3"><DetailSectionLayout /></div>
    <div class="col-span-1"><SummarySectionLayout /></div>
    <div class="col-span-1"></div>
  </div> -->
</template>
