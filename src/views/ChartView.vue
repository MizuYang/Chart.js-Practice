<template>
  <div class="w-60 py-5">
    <div class="row g-5">
      <div class="col-3">
        <h3>Chart 直線圖</h3>
        <ChartView />
      </div>
      <div class="col-3">
        <h3>Chart 直線圖</h3>
        <ChartTwo />
      </div>
      <div class="col-3">
        <h4>Doughnut & Pie Charts 甜甜圈</h4>
        <Doughnut />
      </div>
      <div class="col-3">
        <h3>Bubble Chart 泡泡圖</h3>
        <Bubble />
      </div>
    </div>

    <hr />

    <div class="row g-5">
      <div class="col-3">
        <h3>Line Chart 折線圖</h3>
        <Line />
      </div>
      <div class="col-3">
        <h3>Polar Area Chart 極地區域圖</h3>
        <PolarArea />
      </div>
      <div class="col-3">
        <h3>Radar Chart 雷達圖</h3>
        <Radar />
      </div>
      <div class="col-3">
        <h3>Scatter Chart 散點圖</h3>
        <Scatter />
      </div>
    </div>
  </div>
</template>

<script>
import ChartView from '@/components/BarChart.vue'
import ChartTwo from '@/components/BarChartTwo.vue'
import Doughnut from '@/components/DoughnutChart.vue'
import Bubble from '@/components/BubbleView.vue'
import Line from '@/components/LineChart.vue'
import PolarArea from '@/components/PolarArea.vue'
import Radar from '@/components/RadarChart.vue'
import Scatter from '@/components/ScatterChart.vue'

export default {
  components: {
    ChartView,
    ChartTwo,
    Doughnut,
    Bubble,
    Line,
    PolarArea,
    Radar,
    Scatter
  }
}
</script>

<style lang="scss" scoped>
.w-60 {
  width: 60%;
  margin: 0 auto;
}
h3{
  text-align: center;
}
</style>
