<script>
import { Line } from 'vue-chartjs'

export default {
   extends: Line,
  props: {
    label: {
      type: Array
    },
    chartData: {
      type: Array
    },
    options: {
      type: Object
    },
    colors: {
      type: Array
    }
  },
  mounted () {
    this.renderChart(
      {
        labels: [...Array(52).keys()],
        datasets: [
          {
            label: this.label[0],
            data: this.chartData[0],
            backgroundColor: this.colors[0],
          },
           {
            label: this.label[1],
            data: this.chartData[1],
            backgroundColor: this.colors[1],
          },
           {
            label: this.label[2],
            data: this.chartData[2],
            backgroundColor: this.colors[2],
          },
           {
            label: this.label[3],
            data: this.chartData[3],
            backgroundColor: this.colors[3],
          }
        ]
      },
      this.options
    );
  }
}
</script>