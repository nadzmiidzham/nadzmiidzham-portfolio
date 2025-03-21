<script setup>
import { Disclosure, DisclosureButton, DisclosurePanel } from "@headlessui/vue";
import DownloadCVButton from "../components/DownloadCVButton.vue";
import Avatar from "../components/Avatar.vue";
import SkillSummarySection from "../sections/SkillSummarySection.vue";
</script>

<template>
  <!-- mobile view -->
  <div class="my-3 flex flex-col gap-2 md:hidden">
    <div class="mx-auto"><Avatar /></div>
    <div class="mx-3"><DownloadCVButton /></div>

    <Disclosure v-slot="{ open }">
      <DisclosureButton
        v-if="open"
        class="mx-3 rounded-2xl bg-yellow-400 px-3 py-2 text-center text-green-950 outline"
      >
        <b>Skill Summary</b>
      </DisclosureButton>
      <DisclosureButton
        v-else
        class="mx-3 rounded-2xl bg-green-950 px-3 py-2 text-center text-white"
      >
        <b>Skill Summary</b>
      </DisclosureButton>

      <DisclosurePanel>
        <div class="mx-7"><SkillSummarySection /></div>
      </DisclosurePanel>
    </Disclosure>
  </div>

  <!-- desktop view -->
  <div class="my-3 hidden flex-col gap-3 md:flex">
    <div class="mx-3 flex justify-center">
      <Avatar />
    </div>

    <div class="mx-3">
      <DownloadCVButton />
    </div>

    <div class="mx-auto">
      <div class="mx-10 rounded-2xl bg-yellow-400 text-green-950 outline">
        <h1 class="text-center uppercase">
          <b>Skill Summary</b>
        </h1>
      </div>

      <div class="py-3">
        <SkillSummarySection />
      </div>
    </div>
  </div>
</template>
