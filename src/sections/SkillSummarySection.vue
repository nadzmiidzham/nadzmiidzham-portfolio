<script setup lang="ts">
import ProficiencyScaleBar from "../components/ProficiencyScaleBar.vue";

const programmingLanguageList = [
  { label: "Javascript / Typescript", value: 9, iconPathList: ['images/icons8-javascript.svg','images/icons8-typescript.svg'] },
  { label: "Python", value: 8, iconPathList: ['images/icons8-python.svg'] },
  { label: "PHP", value: 9, iconPathList: ['images/icons8-python.svg'] },
  { label: "Java / Kotlin", value: 8, iconPathList: ['images/icons8-java.svg'] },
];

const frameworkList = [
  { label: "NestJS", value: 9, iconPathList: ['images/icons8-nestjs.svg'] },
  { label: "NuxtJS", value: 8, iconPathList: ['images/icons8-nuxt-js.svg'] },
  { label: "Laravel", value: 9, iconPathList: ['images/icons8-python.svg'] },
  { label: "Slim Framework", value: 9, iconPathList: ['images/icons8-python.svg'] },
  { label: "Flutter", value: 7, iconPathList: ['images/icons8-python.svg'] },
];

const devopToolList = [
  { label: "Docker", value: 9, iconPathList: ['images/icons8-python.svg'] },
  { label: "Gitlab CI/CD", value: 8, iconPathList: ['images/icons8-python.svg'] },
  { label: "ArgoCD", value: 6, iconPathList: ['images/icons8-python.svg'] },
];
</script>

<template>
  <div class="flex flex-col gap-10 py-3">
    <!-- Programming Language -->
    <div>
      <h1><b>Programming Language</b></h1>

      <div v-for="item in programmingLanguageList">
        <ProficiencyScaleBar :value="item.value">
          <template #icon>
            <img v-for="iconPath in item.iconPathList" :src="iconPath" class="w-6 h-6" />
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
            <img v-for="iconPath in item.iconPathList" :src="iconPath" class="w-6 h-6" />
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
            <img v-for="iconPath in item.iconPathList" :src="iconPath" class="w-6 h-6" />
          </template>
          <template #label>
            {{ item.label }}
          </template>
        </ProficiencyScaleBar>
      </div>
    </div>
  </div>
</template>
