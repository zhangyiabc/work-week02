<template>
  <div class="user">
    <h2>个人中心</h2>
    <Echarts type="bar" msg="vue中使用Echarts"/>
    <!-- <Not /> -->
  </div>
</template>

<script>
// import Not from "./404"
import Echarts from "@/components/Echarts"
export default {
  components:{
    Echarts,
    // Not
  }
}
</script>

<style>

</style>