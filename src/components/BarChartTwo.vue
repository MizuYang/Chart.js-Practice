<template>
  <canvas id="myChart2" width="400" height="400"></canvas>
</template>

<script>
import Chart from 'chart.js/auto'
export default {

  mounted () {
    const ctx = document.getElementById('myChart2')

    const myChart2 = new Chart(ctx, { // eslint-disable-line
      type: 'bar',
      data: {
        labels: ['二月', '四月', '六月', '八月', '十月', '十二月'],
        datasets: [{
          label: '# of Votes',
          data: [12, 14, 3, 5, 2, 3],
          backgroundColor: [
            'rgba(255, 99, 132, 0.2)'
          ],
          borderColor: [
            'rgba(255, 99, 132, 1)'
          ],
          borderWidth: 1
        },
        {
          label: '# of Votes',
          data: [15, 9, 5, 15, 5, 15],
          backgroundColor: [
            'rgba(54, 162, 235, 0.2)'
          ],
          borderColor: [
            'rgba(54, 162, 235, 1)'
          ],
          borderWidth: 1
        }]
      },
      options: {
        scales: {
          y: {
            beginAtZero: true
          }
        }
      }
    })
  }

}
</script>
