<script setup>
import { Disclosure, DisclosureButton, DisclosurePanel } from "@headlessui/vue";
import InternshipSection from "../sections/InternshipSection.vue";
import EducationSection from "../sections/EducationSection.vue";
import ExperienceSection from "../sections/ExperienceSection.vue";
import SkillSection from "../sections/SkillSection.vue";
</script>

<template>
  <!-- mobile view -->
  <div class="flex flex-col gap-3 py-3 md:hidden">
    <!-- experience section -->
    <div class="px-3">
      <Disclosure v-slot="{ open }">
        <DisclosureButton
          v-if="!open"
          class="mx-auto w-full rounded-2xl bg-green-950 px-3 py-2"
        >
          <h1 class="text-center text-white uppercase">
            <b>Experience</b>
          </h1>
        </DisclosureButton>
        <DisclosureButton
          v-else
          class="mx-auto w-full rounded-2xl bg-yellow-400 px-3 py-2 text-green-950 outline"
        >
          <h1 class="text-center uppercase">
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
        <DisclosureButton
          v-if="!open"
          class="mx-auto w-full rounded-2xl bg-green-950 px-3 py-2"
        >
          <h1 class="text-center text-white uppercase">
            <b>Internship</b>
          </h1>
        </DisclosureButton>
        <DisclosureButton
          v-else
          class="mx-auto w-full rounded-2xl bg-yellow-400 px-3 py-2 text-green-950 outline"
        >
          <h1 class="text-center uppercase">
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
        <DisclosureButton
          v-if="!open"
          class="mx-auto w-full rounded-2xl bg-green-950 px-3 py-2"
        >
          <h1 class="text-center text-white uppercase">
            <b>Education</b>
          </h1>
        </DisclosureButton>
        <DisclosureButton
          v-else
          class="mx-auto w-full rounded-2xl bg-yellow-400 px-3 py-2 text-green-950 outline"
        >
          <h1 class="text-center uppercase">
            <b>Education</b>
          </h1>
        </DisclosureButton>

        <DisclosurePanel class="py-3">
          <EducationSection />
        </DisclosurePanel>
      </Disclosure>
    </div>

    <!-- skill section -->
    <div class="px-3">
      <div
        class="mx-auto w-full rounded-2xl bg-yellow-400 px-3 py-2 text-green-950 outline"
      >
        <h1 class="text-center uppercase">
          <b>Skill / Tool</b>
        </h1>
      </div>
      <div class="py-3">
        <SkillSection />
      </div>
    </div>
  </div>

  <!-- desktop view -->
  <div class="hidden flex-col gap-3 py-3 md:flex">
    <!-- experience section -->
    <div class="px-3">
      <div
        class="mx-auto w-full rounded-2xl bg-yellow-400 px-3 py-2 text-green-950 outline"
      >
        <h1 class="text-center uppercase">
          <b>Experience</b>
        </h1>
      </div>
      <div class="py-3">
        <ExperienceSection />
      </div>
    </div>

    <!-- internship section -->
    <div class="px-3">
      <div
        class="mx-auto w-full rounded-2xl bg-yellow-400 px-3 py-2 text-green-950 outline"
      >
        <h1 class="text-center uppercase">
          <b>Internship</b>
        </h1>
      </div>
      <div class="py-3">
        <InternshipSection />
      </div>
    </div>

    <!-- education section -->
    <div class="px-3">
      <div
        class="mx-auto w-full rounded-2xl bg-yellow-400 px-3 py-2 text-green-950 outline"
      >
        <h1 class="text-center uppercase">
          <b>Education</b>
        </h1>
      </div>
      <div class="py-3">
        <EducationSection />
      </div>
    </div>

    <!-- skill section -->
    <div class="px-3">
      <div
        class="mx-auto w-full rounded-2xl bg-yellow-400 px-3 py-2 text-green-950 outline"
      >
        <h1 class="text-center uppercase">
          <b>Skill / Tool</b>
        </h1>
      </div>
      <div class="py-3">
        <SkillSection />
      </div>
    </div>
  </div>
</template>
