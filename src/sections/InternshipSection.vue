<script setup>
import TimeLineInfo from "../components/TimeLineInfo.vue";
</script>

<template>
  <TimeLineInfo :isStartTime="true">
    <template #time>2017</template>
    <template #label>UNICEF</template>
    <template #description>
      <h1><b>Intern Game Developer</b></h1>
      <p class="ml-3 text-justify">
          <u>Carbon Game (POC)</u>: Lead the development of an Android mobile game for children to learn about the carbon element up to the end of the POC stage.
      </p>
    </template>
  </TimeLineInfo>
</template>
