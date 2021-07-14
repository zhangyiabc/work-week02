<template>
  <div class="not-found">
    <div class="container">
      <img ref="img" src="../../assets/404.gif" alt="" />
    </div>
  </div>
</template>

<script>
// import gif from "@/assets/404.gif"
export default {};
</script>

<style lang="scss" scoped>
.not-found {
  box-sizing: border-box;
  width: 100vw;
  height: 100vh;
  div {
    width: 100%;
    height: 100%;
    img{
      width: 80%;
    }
  }
}
</style>