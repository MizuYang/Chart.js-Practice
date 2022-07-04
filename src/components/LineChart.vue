<template>
  <canvas id="line" width="400" height="400"></canvas>
</template>

<script>
import Chart from 'chart.js/auto'
export default {

  data () {
    return {
    }
  },
  mounted () {
    const ctx = document.getElementById('line')

    const labels = ['1月', '2月', '3月', '4月', '5月', '6月', '7月']
    const data = {
      labels: labels,
      datasets: [{
        label: 'My First Dataset',
        data: [65, 59, 80, 81, 56, 55, 40],
        fill: false,
        borderColor: 'rgb(75, 192, 192)',
        tension: 0.1
      }]
    }
    const line = new Chart(ctx, { // eslint-disable-line
      type: 'line',
      data: data
    })
  }

}
</script>

<style lang='scss' scope></style>
