<template>
  <canvas id="scatter" width="400" height="400"></canvas>
</template>

<script>
import Chart from 'chart.js/auto'
export default {

  mounted () {
    const ctx = document.getElementById('scatter')

    const data = {
      datasets: [{
        label: 'Scatter Dataset',
        data: [{
          x: -10,
          y: 0
        }, {
          x: -5,
          y: 3
        }, {
          x: 10,
          y: 5
        }, {
          x: 0.5,
          y: 5.5
        }],
        backgroundColor: 'rgb(255, 99, 132)'
      }]
    }
    const scatter = new Chart(ctx, { // eslint-disable-line
      type: 'scatter',
      data: data,
      options: {
        scales: {
          x: {
            type: 'linear',
            position: 'bottom'
          }
        }
      }
    })
  }

}
</script>
