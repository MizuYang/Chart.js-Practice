<template>
  <canvas id="doughnut" width="400" height="400"></canvas>
</template>

<script>
import Chart from 'chart.js/auto'
export default {

  mounted () {
    const ctx = document.getElementById('doughnut')

    const data = {
      labels: [
        'Red',
        'Blue',
        'Yellow'
      ],
      datasets: [{
        label: 'My First Dataset',
        data: [300, 50, 100],
        backgroundColor: [
          'rgb(255, 99, 132)',
          'rgb(54, 162, 235)',
          'rgb(255, 205, 86)'
        ],
        hoverOffset: 4
      }]
    }
    const doughnut = new Chart(ctx, { // eslint-disable-line
      type: 'doughnut',
      data: data
    })
  }

}
</script>
