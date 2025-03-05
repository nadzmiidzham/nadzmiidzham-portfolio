<script setup>
import {
  Disclosure,
  DisclosureButton,
  DisclosurePanel,
} from '@headlessui/vue'
import DownloadCVButton from "../components/DownloadCVButton.vue";
import Avatar from "../components/Avatar.vue";
import SkillSummarySection from "../sections/SkillSummarySection.vue";
</script>

<template>
  <div class="flex flex-col gap-2 my-3">
    <div class="mx-auto"><Avatar /></div>
    <div class="mx-3"><DownloadCVButton /></div>
    
    <Disclosure>
      <DisclosureButton class="mx-3 rounded-2xl bg-yellow-400 py-2 px-3 text-center text-green-950 outline">
        <b>Skill Summary</b>
      </DisclosureButton>

      <DisclosurePanel>
        <div class="mx-7"><SkillSummarySection /></div>
      </DisclosurePanel>
    </Disclosure>
  </div>
</template>
