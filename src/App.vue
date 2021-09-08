<template>
  <div>
    <line-charts :chartData="DM" :options="chartOptions" label="DM"></line-charts>
  </div>
</template>

<script>

import json from './jstest';
import LineCharts from './components/LineCharts.vue';

export default {
  name: 'App',
  components: {
    LineCharts
  },
  data() {
    return {
      data: json,
      DM: json.DM,
      OOH: json.OOH,
      PPC: json.PPC,
      TV: json.TV,
      chartOptions: {
        responsive: true,
        maintainAspectRatio: false
      }
    }
  },
  computed: {
  }
}
console.log(json)
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>