<script setup lang="ts">
import IconPillButton from "../components/IconPillButton.vue";
import LanguageProficiencyScale from "../components/LanguageProficiencyScale.vue";

const devOpList = [
  {
    label: "Docker",
    iconPath: "/images/docker-icon.svg",
    linkUrl: "https://www.docker.com/",
  },
  {
    label: "Kubernetes",
    iconPath: "/images/kubernetes-icon.svg",
    linkUrl: "https://kubernetes.io/",
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
  {
    label: "AWS",
    iconPath: "/images/aws-icon.svg",
    linkUrl: "https://aws.amazon.com/",
  },
  {
    label: "GCP",
    iconPath: "/images/gcp-icon.svg",
    linkUrl: "https://cloud.google.com/",
  },
  {
    label: "Heroku",
    iconPath: "/images/heroku-icon.svg",
    linkUrl: "https://www.heroku.com/",
  },
  {
    label: "Datadog",
    iconPath: "/images/datadog-icon.svg",
    linkUrl: "https://www.datadoghq.com/",
  },
  {
    label: "Github",
    iconPath: "/images/github-icon.svg",
    linkUrl: "https://github.com/",
  },
  {
    label: "Gitlab",
    iconPath: "/images/gitlab-icon.svg",
    linkUrl: "https://gitlab.com/",
  },
  {
    label: "MessageBird",
    iconPath: "/images/messagebird-icon.svg",
    linkUrl: "https://developers.messagebird.com/",
  },
  {
    label: "MailGun",
    iconPath: "/images/mailgun-icon.svg",
    linkUrl: "https://www.mailgun.com/",
  },
];
const programmingLanguageList = [
  {
    label: "Javascript",
    iconPath: "/images/javascript-icon.svg",
    linkUrl: "https://www.javascript.com/",
  },
  {
    label: "Typescript",
    iconPath: "/images/typescript-icon.svg",
    linkUrl: "https://www.typescriptlang.org/",
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
    label: "Java",
    iconPath: "/images/java-icon.svg",
    linkUrl: "https://www.java.com/en/",
  },
  {
    label: "Kotlin",
    iconPath: "/images/kotlin-icon.svg",
    linkUrl: "https://kotlinlang.org/",
  },
];
const frameworkList = [
  {
    label: "Node.js",
    iconPath: "/images/nodejs-icon.svg",
    linkUrl: "https://nodejs.org/en",
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
    label: "Codeigniter",
    iconPath: "/images/codeigniter-icon.svg",
    linkUrl: "https://codeigniter.com/",
  },
  {
    label: "Qt Framework (Python)",
    iconPath: "/images/qt-icon.svg",
    linkUrl: "https://doc.qt.io/qtforpython-6/",
  },
];
const otherTool = [
  {
    label: "Vite",
    iconPath: "/vite.svg",
    linkUrl: "https://vite.dev/",
  },
  {
    label: "Linux",
    iconPath: "/images/linux-icon.svg",
    linkUrl: "https://www.linux.org/",
  },
  {
    label: "Arch Linux",
    iconPath: "/images/arch-linux-icon.svg",
    linkUrl: "https://archlinux.org/",
  },
];

const skillList = [
  ...devOpList,
  ...programmingLanguageList,
  ...frameworkList,
  ...otherTool,
];

const languageList = [
  {
    label: "Malay",
    value: 9,
    iconPathList: ["images/java-icon.svg"],
  },
  {
    label: "English",
    value: 7,
    iconPathList: ["images/java-icon.svg"],
  },
];
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

  <div class="mx-auto">
    <div class="mx-20 my-3 rounded-2xl bg-yellow-400 text-green-950 outline">
      <h1 class="text-center uppercase">
        <b>Language</b>
      </h1>
    </div>

    <div class="mx-7 rounded-md bg-yellow-200 p-3 outline outline-yellow-600">
      <LanguageProficiencyScale
        v-for="item in languageList"
        :value="item.value"
      >
        <template #icon>
          <img
            v-for="iconPath in item.iconPathList"
            :src="iconPath"
            class="h-6 w-6"
          />
        </template>
        <template #label>
          <b class="uppercase">{{ item.label }}</b>
        </template>
      </LanguageProficiencyScale>
    </div>
  </div>
</template>
