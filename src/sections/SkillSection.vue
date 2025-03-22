<script setup lang="ts">
import IconPillButton from "../components/IconPillButton.vue";

const devOpList = [
  {
    label: "Docker",
    iconPath: "/images/docker-icon.svg",
    linkUrl: "https://www.docker.com/",
  },
  {
    label: "Gitlab CI/CD",
    iconPath: "/images/gitlab-icon.svg",
    linkUrl: "https://docs.gitlab.com/ci/",
  },
  {
    label: "Argo CD",
    iconPath: "/images/argocd-icon.svg",
    linkUrl: "https://argoproj.github.io/cd/",
  },
];
const programmingLanguageList = [
  {
    label: "Java",
    iconPath: "/images/java-icon.svg",
    linkUrl: "https://www.java.com/en/",
  },
  {
    label: "Javascript",
    iconPath: "/images/javascript-icon.svg",
    linkUrl: "https://www.javascript.com/",
  },
  {
    label: "Kotlin",
    iconPath: "/images/kotlin-icon.svg",
    linkUrl: "https://kotlinlang.org/",
  },
  {
    label: "PHP",
    iconPath: "/images/php-icon.svg",
    linkUrl: "https://www.php.net/",
  },
  {
    label: "Python",
    iconPath: "/images/python-icon.svg",
    linkUrl: "https://www.python.org/",
  },
  {
    label: "Typescript",
    iconPath: "/images/typescript-icon.svg",
    linkUrl: "https://www.typescriptlang.org/",
  },
];
const frameworkList = [
  {
    label: "Flutter",
    iconPath: "/images/flutter-icon.svg",
    linkUrl: "https://flutter.dev/",
  },
  {
    label: "Laravel",
    iconPath: "/images/laravel-icon.svg",
    linkUrl: "https://laravel.com/",
  },
  {
    label: "NestJs",
    iconPath: "/images/nestjs-icon.svg",
    linkUrl: "https://nestjs.com/",
  },
  {
    label: "NuxtJs",
    iconPath: "/images/nuxtjs-icon.svg",
    linkUrl: "https://nuxt.com/",
  },
];

const skillList = [...devOpList, ...programmingLanguageList, ...frameworkList];
</script>

<template>
  <div class="mx-7 flex flex-wrap justify-center gap-1">
    <IconPillButton
      v-for="skill in skillList"
      :label="skill.label"
      :iconPath="skill.iconPath"
      :linkUrl="skill.linkUrl"
    />
  </div>
</template>
