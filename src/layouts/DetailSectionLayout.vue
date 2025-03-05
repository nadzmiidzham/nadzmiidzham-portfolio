<script setup>
import {
  Disclosure,
  DisclosureButton,
  DisclosurePanel,
} from '@headlessui/vue';
import InternshipSection from '../sections/InternshipSection.vue';
import EducationSection from '../sections/EducationSection.vue';
import ExperienceSection from '../sections/ExperienceSection.vue';
</script>

<template>
  <div class="flex flex-col gap-3 py-3">
    <!-- experience section -->
    <div class="px-3">
      <Disclosure v-slot="{ open }">
        <DisclosureButton v-if="!open" class="mx-auto w-full py-2 px-3 rounded-2xl bg-green-950">
          <h1 class="uppercase text-center text-white">
            <b>Experience</b>
          </h1>
        </DisclosureButton>
        <DisclosureButton v-else class="mx-auto w-full py-2 px-3 rounded-2xl bg-yellow-400 text-green-950 outline">
          <h1 class="uppercase text-center">
            <b>Experience</b>
          </h1>
        </DisclosureButton>

        <DisclosurePanel class="py-3">
          <ExperienceSection />
        </DisclosurePanel>
      </Disclosure>
    </div>

    <!-- internship section -->
    <div class="px-3">
      <Disclosure v-slot="{ open }">
        <DisclosureButton v-if="!open" class="mx-auto w-full py-2 px-3 rounded-2xl bg-green-950">
          <h1 class="uppercase text-center text-white">
            <b>Internship</b>
          </h1>
        </DisclosureButton>
        <DisclosureButton v-else class="mx-auto w-full py-2 px-3 rounded-2xl bg-yellow-400 text-green-950 outline">
          <h1 class="uppercase text-center">
            <b>Internship</b>
          </h1>
        </DisclosureButton>

        <DisclosurePanel class="py-3">
          <InternshipSection />
        </DisclosurePanel>
      </Disclosure>
    </div>

    <!-- education section -->
    <div class="px-3">
      <Disclosure v-slot="{ open }">
        <DisclosureButton v-if="!open" class="mx-auto w-full py-2 px-3 rounded-2xl bg-green-950">
          <h1 class="uppercase text-center text-white">
            <b>Education</b>
          </h1>
        </DisclosureButton>
        <DisclosureButton v-else class="mx-auto w-full py-2 px-3 rounded-2xl bg-yellow-400 text-green-950 outline">
          <h1 class="uppercase text-center">
            <b>Education</b>
          </h1>
        </DisclosureButton>

        <DisclosurePanel class="py-3">
          <EducationSection />
        </DisclosurePanel>
      </Disclosure>
    </div>
  </div>
</template>
