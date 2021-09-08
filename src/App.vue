<template>
  <div>
    <h1>Data Visualization</h1>
    <line-charts :chartData="[DM, OOH, PPC, TV]" :options="chartOptions" :label="labels" :colors="colors"></line-charts>
  </div>
</template>

<script>

import json from './jstest';
import LineCharts from './components/Chart.vue';

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
      },
      labels: ["DM", "OOH", "PPC", "TV"],
      colors: ["green", "yellow", "blue", "red"]
    }
  },
  computed: {
  }
}
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
body {
  background-color: lightblue;
}
h1 {
  color: royalblue;
  text-align: center;
}
</style>