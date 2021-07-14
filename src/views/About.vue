<template>
  <div class="about">
    <h1>This is an about page</h1>
    <Echarts h="450px" w="800px" :tableData="dataArray" :msg="tableMsg" :tableName="nameArray" />
  </div>
</template>

<script>
import Echarts from "@/components/Echarts";
export default {
  components: {
    Echarts,
  },
  data() {
    return {
      dataArray: [12, 15, 18, 10, 6, 9, 20],
      nameArray: ["周一", "周二", "周三", "周四", "周五", "周六", "周日"],
      tableMsg: "一周的统计图表",
    };
  },
};
</script>

<style lang="scss" scoped>
.about {
  // width: ;
  height: 400px;
  text-align: center;
}
</style>

