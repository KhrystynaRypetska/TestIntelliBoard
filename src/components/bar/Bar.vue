<template>
  <div class="bar">
    <h2 class="gl-title-block title">Paid Customers vs. All Registrans by platform</h2>
    <div class="bar_content">
      <div class="bar_content_item">
        <canvas ref="canvas"></canvas>
      </div>
      <div class="bar_content_item">
        <ul class="bar_list">
          <li class="bar_list_item">
            <span class="title">Customer Growth:</span>
          </li>
          <li class="bar_list_item">
            <span class="text">Blackboard Learn</span>
            <span class="button">40%</span>
          </li>
          <li class="bar_list_item">
            <span class="text">2DL</span>
            <span class="button">10%</span>
          </li>
          <li class="bar_list_item">
            <span class="text">Canvas</span>
            <span class="button">32%</span>
          </li>
          <li class="bar_list_item">
            <span class="text">Moodle</span>
            <span class="button">50%</span>
          </li>
        </ul>
      </div>
    </div>

  </div>
</template>

<style lang="scss" scoped>
@import "Bar.scss";
</style>
<script>
import { Bar } from 'vue-chartjs'
export default  {
  name: 'Doughnut',
  extends: Bar,
  data: () => ({
    chartdata: {
      labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
      datasets: [{
        label: '# of Votes',
        data: [12, 19, 3, 5, 2, 3],
        backgroundColor: [
          'rgba(255, 99, 132, 0.2)',
          'rgba(54, 162, 235, 0.2)',
          'rgba(255, 206, 86, 0.2)',
          'rgba(75, 192, 192, 0.2)',
          'rgba(153, 102, 255, 0.2)',
          'rgba(255, 159, 64, 0.2)'
        ],
        borderColor: [
          'rgba(255, 99, 132, 1)',
          'rgba(54, 162, 235, 1)',
          'rgba(255, 206, 86, 1)',
          'rgba(75, 192, 192, 1)',
          'rgba(153, 102, 255, 1)',
          'rgba(255, 159, 64, 1)'
        ],
        borderWidth: 1
      }]
    },
    options: {
      responsive: true,
      maintainAspectRatio: false
    }
  }),
  mounted () {
    this.renderChart(this.chartdata, this.options)
  },
}
</script>