<template>
  <div class="histogram">

    <h2 class="gl-title-block title">Sales by product</h2>
    <div class="histogram_content">
      <div class="histogram_content_item">
        <canvas ref="canvas"></canvas>
      </div>
      <div class="histogram_content_item">
        <ul class="histogram_list">
          <li class="histogram_list_item">
            <span class="title">Product growth:</span>
          </li>
          <li class="histogram_list_item">
            <span class="button blueCollor"></span>
           <span class="text">IntelliBoard</span>
            <span class="number">40%</span>
          </li>
          <li class="histogram_list_item">
            <span class="button blueLightCollor"></span>
            <span class="text">IntelliCart</span>
            <span class="number">10%</span>
          </li>
          <li class="histogram_list_item">
            <span class="button orangCollor"></span>
            <span class="text">InAttedance</span>
            <span class="number">32%</span>
          </li>
          <li class="histogram_list_item">
            <span class="button greenCollor"></span>
            <span class="text">AYS Onboard</span>
            <span class="number">50%</span>
          </li>
          <li class="histogram_list_item">
            <span class="button pinckCollor"></span>
            <span class="text">AYS Evolve</span>
            <span class="number">50%</span>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import "Histogram.scss";
</style>

<script>
import { Doughnut } from 'vue-chartjs'
export default  {
name: 'Histogram',
  extends: Doughnut,
  data: () => ({
    chartdata: {
        datasets: [{
          data: [40, 10, 32, 50, 50],
          backgroundColor: [
            '#A8BDFF',
            '#123CE1',
            '#FF7ADA',
            '#64D60B',
            '#FFB800'
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
  // methods: {
  //   renderChart() {
  //     this.chartdata = {
  //       labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
  //       datasets: [{
  //         label: '# of Votes',
  //         data: [12, 19, 3, 5, 2, 3],
  //         backgroundColor: [
  //           'rgba(255, 99, 132, 0.2)',
  //           'rgba(54, 162, 235, 0.2)',
  //           'rgba(255, 206, 86, 0.2)',
  //           'rgba(75, 192, 192, 0.2)',
  //           'rgba(153, 102, 255, 0.2)',
  //           'rgba(255, 159, 64, 0.2)'
  //         ],
  //         borderColor: [
  //           'rgba(255, 99, 132, 1)',
  //           'rgba(54, 162, 235, 1)',
  //           'rgba(255, 206, 86, 1)',
  //           'rgba(75, 192, 192, 1)',
  //           'rgba(153, 102, 255, 1)',
  //           'rgba(255, 159, 64, 1)'
  //         ],
  //         borderWidth: 1
  //       }]
  //     }
  //     this.option = {
  //       scales: {
  //         yAxes: [{
  //           ticks: {
  //             beginAtZero: true
  //           }
  //         }]
  //       }
  //     }
  //   }
  // }
}
</script>