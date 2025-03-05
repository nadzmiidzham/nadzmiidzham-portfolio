<script setup>
import TimeLineInfo from "../components/TimeLineInfo.vue";
</script>

<template>
  <div class="flex flex-col gap-3">
    <TimeLineInfo>
      <template #time>2018</template>
      <template #label>Bachelor</template>
      <template #description>
        <h1><b>Bachelor in Computer Science (Hons.)</b></h1>
        <h5>UiTM Shah Alam (Selangor, Malaysia)</h5>
      </template>
    </TimeLineInfo>
    
    <TimeLineInfo>
      <template #time>2015</template>
      <template #label>Diploma</template>
      <template #description>
        <h1><b>Diploma in Computer Science</b></h1>
        <h5>UiTM Merbok (Kedah, Malaysia)</h5>
      </template>
    </TimeLineInfo>
    
    <TimeLineInfo :showTimelineTrail="false">
      <template #time>2013</template>
      <template #label>O-Level</template>
      <template #description>
        <h1><b>Sijil Pelajaran Malaysia (SPM)</b></h1>
        <h5>Royal Military College (Kuala Lumpur, Malaysia)</h5>
      </template>
    </TimeLineInfo>
  </div>
</template>
