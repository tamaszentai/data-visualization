<template>
  <div>
    <Header/>
    <h1>Data Visualization</h1>
    <chart
      :chartData="[DM, OOH, PPC, TV]"
      :options="chartOptions"
      :label="labels"
      :colors="colors"
    ></chart>
  </div>
</template>

<script>
import json from "./jstest";
import Header from "./components/Header.vue";
import Chart from "./components/Chart.vue";

export default {
  name: "App",
  components: {
    Header,
    Chart,
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
        maintainAspectRatio: false,
      },
      labels: ["DM", "OOH", "PPC", "TV"],
      colors: ["green", "yellow", "blue", "red"],
    };
  },
};
</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
body {
  font-family: 'Roboto', sans-serif;
  background-color: lightblue;
  margin: 0;
  padding: 0;
}
h1 {
  color: royalblue;
  text-align: center;
}
</style>