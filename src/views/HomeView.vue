<script setup lang="ts">
import { Job } from 'src/types/Job'
import { ref } from 'vue';

const jobList = ref<Job[]>([
  { title: 'farm worker', location: 'lon lon ranch', salary: 30000, id: '1' },
  { title: 'quarryman', location: 'death mountain', salary: 40000, id: '2' },
  { title: 'flute player', location: 'the lost woods', salary: 35000, id: '3' },
  { title: 'fisherman', location: 'lake hylia', salary: 21000, id: '4' },
  { title: 'prison guard', location: 'gerudo valley', salary: 32000, id: '5' }
])
</script>

<template>
  <div id="HomeView">
    <h1 v-for="item in jobList" :key="item.id">{{ item.title }}</h1>
  </div>
</template>

<style lang="scss" scoped>
#HomeView {}
</style>
