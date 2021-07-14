<template>
  <div class="echarts-container">
    <div :style="{ height: h, width: w }" ref="myChart"></div>
  </div>
</template>

<script>
export default {
  name: "Echars",
  props: {
    // 图表的高度
    h: {
      type: String,
      default: "400px",
    },
    // 图表的宽度
    w: {
      type: String,
      default: "600px",
    },
    // 图表标题
    msg: {
      type: String,
      default: "这是图表的标题",
    },
    // 图表数据
    tableData: {
      type: Array,
      default: () => [1, 10, 12, 45, 50, 14],
    },
    // 图表数据名
    tableName: {
      type: Array,
      default: () => ["衬衫", "羊毛衫", "雪纺衫", "裤子", "高跟鞋", "袜子"],
    },
    // 图表类型
    type: {
      type: String,
      default: "line",
    },
  },
  data() {
    return {};
  },
  mounted() {
    this.drawLine();
  },
  methods: {
    drawLine() {
      // 基于准备好的dom，初始化echarts实例
      let myChart = this.$echarts.init(this.$refs.myChart);
      // 绘制图表
      myChart.setOption({
        title: { text: this.msg },
        tooltip: {},
        xAxis: {
          data: this.tableName,
        },
        yAxis: {},
        series: [
          {
            name: "销量",
            type: this.type,
            data: this.tableData,
          },
        ],
      });
    },
  },
};
</script>

<style lang="scss" scoped>
.echarts-container {
  div {
    position: relative;
    margin: 0 auto;
  }
}
</style>

