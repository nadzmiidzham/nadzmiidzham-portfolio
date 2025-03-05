<script setup>
import TimeLineInfo from "../components/TimeLineInfo.vue";
</script>

<template>
  <div class="flex flex-col">
    <!-- carsome -->
    <TimeLineInfo>
      <template #time>10/2019 - 05/2024</template>
      <template #label>Carsome</template>
      <template #description>
        <h1><b>Lead Software Engineer</b></h1>
        <ul class="ml-3 list-inside list-image-[url('images/tick.svg')]">
          <li class="text-justify">
            Migrated cloud services from AWS to Google GCP and revamped the CI/CD pipeline using Gitlab CI and ArgoCD.
          </li>
          <li class="text-justify">
            Implemented a pull-based DevOps pipeline to enhance QA testing and reduce costs.
          </li>
          <li class="text-justify">
            Created "Review App" environments dynamically to streamline testing and deployment processes.
          </li>
        </ul>

        <h1><b>Lead Software Engineer</b></h1>
        <ul class="ml-3 list-inside list-image-[url('images/tick.svg')]">
          <li class="text-justify">
            Spearheaded the development of a car pricing tool (<u>Buyer Tool</u>) that improved inspection efficiency by 80% in Indonesia.
          </li>
          <li class="text-justify">
            Reduced customer wait time for car valuations significantly.
          </li>
        </ul>

        <h1><b>Senior Web Developer</b></h1>
        <ul class="ml-3 list-inside list-image-[url('images/tick.svg')]">
          <li class="text-justify">
            Developed Lead Microservice (Lead MS) integrated with Zoho CRM and revamped Carsome's website to incorporate Lead MS.
          </li>
          <li class="text-justify">
            Initiated a Notification Microservice (POC) to decouple notification handling from existing modules.
          </li>
        </ul>

        <h1><b>Junior Web Developer</b></h1>
        <p class="ml-3 text-justify">
          Maintained Carsome CMS and introduced a Watchlist Microservice POC for the internal bidding system.
        </p>
      </template>
    </TimeLineInfo>
    
    <!-- strateq -->
    <TimeLineInfo>
      <template #time>10/2018 - 10/2019</template>
      <template #label>Starteq</template>
      <template #description>
        <h1><b>R&D Engineer</b></h1>
        <ul class="ml-3 list-inside list-image-[url('images/tick.svg')]">
          <li class="text-justify">
            Led the Data Migration team and integrated StrateqEHR with Waystar Zirmed.
          </li>
          <li class="text-justify">
            Designed a data migration template for new tenants of StrateqEHR.
          </li>
        </ul>

        <h1><b>Junior Web Developer</b></h1>
        <p class="ml-3 text-justify">
          Enhanced and maintained 37Degrees HIS (Asia) and StrateqEHR (US) systems.
        </p>
      </template>
    </TimeLineInfo>
    
    <!-- freelance -->
    <TimeLineInfo :isStartTime="true">
      <template #time>03/2017 - 08/2018</template>
      <template #label>Freelance</template>
      <template #description>
        <h1><b>Android Mobile App Developer</b></h1>

        <h2>
          <u><b>UiTM Shah Alam</b></u>
        </h2>
        <ul class="ml-3 list-inside list-image-[url('images/tick.svg')]">
          <li class="text-justify">
            Developed UiTM E-Traffic Summon (UeTS), an award-winning project to improve student vehicle summoning systems.
          </li>
          <li class="text-justify">
            Created Central Tendency Snapshot (CTS), an educational app for Calculus students using OCR technology.
          </li>
        </ul>

        <h2>
          <u><b>Onepage Media Networks</b></u>
        </h2>
        <p class="ml-3 text-justify">
          Built Android apps to support company marketing events, featuring recipes and lucky draw functionalities.
        </p>
      </template>
    </TimeLineInfo>
  </div>
</template>
