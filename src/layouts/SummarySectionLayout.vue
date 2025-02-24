<script setup lang="ts">
import DownloadCVButton from "../components/DownloadCVButton.vue";
import Avatar from "../components/Avatar.vue";
import SkillSummarySection from "../sections/SkillSummarySection.vue";
</script>

<template>
  <div class="flex flex-col gap-2">
    <div class="m-auto"><Avatar /></div>
    <div class="m-auto"><DownloadCVButton /></div>
    <div class="mx-10"><SkillSummarySection /></div>
  </div>
  <!-- <div class="flex flex-col gap-2">
    <Avatar />
    <DownloadCVButton />
    <SkillSummarySection />
  </div> -->
</template>
