<script>
import { Line } from 'vue-chartjs'

export default {
   extends: Line,
  props: {
    label: {
      type: String
    },
    chartData: {
      type: Array
    },
    options: {
      type: Object
    }
  },
  mounted () {
    this.renderChart(
      {
        labels: this.chartData,
        datasets: [
          {
            label: this.label,
            data: this.chartData
          }
        ]
      },
      this.options
    );
  }
}
</script>