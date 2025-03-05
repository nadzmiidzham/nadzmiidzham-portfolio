<script setup lang="ts">
import InternshipSection from '../sections/InternshipSection.vue';
import EducationSection from '../sections/EducationSection.vue';
import ExperienceSection from '../sections/ExperienceSection.vue';
</script>

<template>
  <div class="flex flex-col gap-3 py-3">
    <div class="px-3">
      <h1 class="uppercase text-green-950 text-center"><b>Experience</b></h1>
      <ExperienceSection />
    </div>
    <div class="px-3">
      <h1 class="uppercase text-green-950 text-center"><b>Internship</b></h1>
      <InternshipSection />
    </div>
    <div class="px-3">
      <h1 class="uppercase text-green-950 text-center"><b>Education</b></h1>
      <EducationSection />
    </div>
  </div>
</template>
