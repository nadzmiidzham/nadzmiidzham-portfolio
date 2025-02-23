<script setup lang="ts">
import ProficiencyScaleBar from "../components/ProficiencyScaleBar.vue";

const programmingLanguageList = [
  { label: "Javascript / Typescript", value: 9 },
  { label: "PHP", value: 9 },
  { label: "Java / Kotlin", value: 8 },
];

const frameworkList = [
  { label: "NestJS", value: 9 },
  { label: "NuxtJS", value: 8 },
  { label: "Laravel", value: 9 },
  { label: "Slim Framework", value: 9 },
  { label: "Flutter", value: 6 },
  { label: "Android Studio (Java / Kotlin)", value: 8 },
];

const devopToolList = [
  { label: "Docker", value: 9 },
  { label: "Gitlab CI/CD", value: 8 },
  { label: "ArgoCD", value: 6 },
];
</script>

<template>
  <div class="py-3">
    <!-- Programming Language -->
    <div>
      <h1><b>Programming Language</b></h1>

      <div v-for="item in programmingLanguageList">
        <ProficiencyScaleBar :label="item.label" :value="item.value" />
      </div>
    </div>

    <!-- framework skill -->
    <div>
      <h1><b>Framework</b></h1>

      <div v-for="item in frameworkList">
        <ProficiencyScaleBar :label="item.label" :value="item.value" />
      </div>
    </div>

    <!-- DevOp Tool -->
    <div>
      <h1><b>DevOp Tool</b></h1>

      <div v-for="item in devopToolList">
        <ProficiencyScaleBar :label="item.label" :value="item.value" />
      </div>
    </div>
  </div>
</template>
