<template>
  <canvas id="bubble" width="400" height="400"></canvas>
</template>

<script>
import Chart from 'chart.js/auto'
export default {

  mounted () {
    const ctx = document.getElementById('bubble')

    const data = {
      datasets: [{
        label: 'First Dataset',
        data: [{
          x: 20,
          y: 14,
          r: 15
        }, {
          x: 40,
          y: 12,
          r: 10
        }, {
          x: 30,
          y: 11,
          r: 25
        },
        {
          x: 25,
          y: 15,
          r: 10
        }
        ],
        backgroundColor: ['rgb(255, 99, 132)', 'rgb(25, 5, 32)', 'rgb(125, 150, 122)', 'rgb(185, 50, 62)']
      }]
    }
    const bubble = new Chart(ctx, { // eslint-disable-line
      type: 'bubble',
      data: data,
      options: {}
    })
  }

}
</script>
