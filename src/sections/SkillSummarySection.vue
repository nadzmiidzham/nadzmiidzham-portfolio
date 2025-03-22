<script setup lang="ts">
import ProficiencyScaleBar from "../components/ProficiencyScaleBar.vue";

const programmingLanguageList = [
  {
    label: "Javascript / Typescript",
    value: 9,
    iconPathList: ["images/javascript-icon.svg", "images/typescript-icon.svg"],
  },
  { label: "Python", value: 8, iconPathList: ["images/python-icon.svg"] },
  { label: "PHP", value: 9, iconPathList: ["images/php-icon.svg"] },
  {
    label: "Java / Kotlin",
    value: 8,
    iconPathList: ["images/java-icon.svg", "images/kotlin-icon.svg"],
  },
];

const frameworkList = [
  { label: "NestJS", value: 9, iconPathList: ["images/nestjs-icon.svg"] },
  { label: "NuxtJS", value: 8, iconPathList: ["images/nuxtjs-icon.svg"] },
  { label: "Laravel", value: 9, iconPathList: ["images/laravel-icon.svg"] },
  { label: "Flutter", value: 7, iconPathList: ["images/flutter-icon.svg"] },
];

const devopToolList = [
  { label: "Docker", value: 9, iconPathList: ["images/docker-icon.svg"] },
  { label: "Gitlab CI/CD", value: 8, iconPathList: ["images/gitlab-icon.svg"] },
  { label: "ArgoCD", value: 6, iconPathList: ["images/argocd-icon.svg"] },
];
</script>

<template>
  <!-- mobile view -->
  <div class="flex flex-col gap-2 rounded-2xl bg-yellow-100 p-3 md:hidden">
    <!-- Programming Language -->
    <div>
      <h1><b>Programming Language</b></h1>

      <div v-for="item in programmingLanguageList">
        <ProficiencyScaleBar :value="item.value">
          <template #icon>
            <img
              v-for="iconPath in item.iconPathList"
              :src="iconPath"
              class="h-6 w-6"
            />
          </template>
          <template #label>
            {{ item.label }}
          </template>
        </ProficiencyScaleBar>
      </div>
    </div>

    <!-- framework skill -->
    <div>
      <h1><b>Framework</b></h1>

      <div v-for="item in frameworkList">
        <ProficiencyScaleBar :value="item.value">
          <template #icon>
            <img
              v-for="iconPath in item.iconPathList"
              :src="iconPath"
              class="h-6 w-6"
            />
          </template>
          <template #label>
            {{ item.label }}
          </template>
        </ProficiencyScaleBar>
      </div>
    </div>

    <!-- DevOp Tool -->
    <div>
      <h1><b>DevOp Tool</b></h1>

      <div v-for="item in devopToolList">
        <ProficiencyScaleBar :value="item.value">
          <template #icon>
            <img
              v-for="iconPath in item.iconPathList"
              :src="iconPath"
              class="h-6 w-6"
            />
          </template>
          <template #label>
            {{ item.label }}
          </template>
        </ProficiencyScaleBar>
      </div>
    </div>
  </div>

  <!-- desktop view -->
  <div class="hidden flex-col gap-2 rounded-xl bg-yellow-100 p-3 md:flex">
    <!-- Programming Language -->
    <div>
      <h1><b>Programming Language</b></h1>

      <div v-for="item in programmingLanguageList" class="min-w-3xs">
        <ProficiencyScaleBar :value="item.value">
          <template #icon>
            <img
              v-for="iconPath in item.iconPathList"
              :src="iconPath"
              class="h-6 w-6"
            />
          </template>
          <template #label>
            {{ item.label }}
          </template>
        </ProficiencyScaleBar>
      </div>
    </div>

    <!-- framework skill -->
    <div>
      <h1><b>Framework</b></h1>

      <div v-for="item in frameworkList" class="min-w-3xs">
        <ProficiencyScaleBar :value="item.value">
          <template #icon>
            <img
              v-for="iconPath in item.iconPathList"
              :src="iconPath"
              class="h-6 w-6"
            />
          </template>
          <template #label>
            {{ item.label }}
          </template>
        </ProficiencyScaleBar>
      </div>
    </div>

    <!-- DevOp Tool -->
    <div>
      <h1><b>DevOp Tool</b></h1>

      <div v-for="item in devopToolList" class="min-w-3xs">
        <ProficiencyScaleBar :value="item.value">
          <template #icon>
            <img
              v-for="iconPath in item.iconPathList"
              :src="iconPath"
              class="h-6 w-6"
            />
          </template>
          <template #label>
            {{ item.label }}
          </template>
        </ProficiencyScaleBar>
      </div>
    </div>
  </div>
</template>
