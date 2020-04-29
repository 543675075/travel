<template>
  <van-swipe class="my-swipe" :autoplay="false" indicator-color="white">
    <van-swipe-item v-for="item in swipe" :key="item.id">
      <img :src="item.src" class="img_bg">
      <img src="../../assets/img/img_wrapper.png" class="img_wrapper">
      <img :src="item.src" class="img_show">
    </van-swipe-item>
  </van-swipe>
</template>



<script>
export default {
  name: "Swipe",
  props:{
    swipe:{
      type: Array,
      default: []
    }
  }
};
</script>
<style lang='less' scoped>
  .my-swipe .van-swipe-item {
    position: relative;
    width: 100vw;
    height: 100vh;
    color: #fff;
    font-size: 20px;
    line-height: 150px;
    // text-align: center;
    // background-color: #39a9ed;
  }
  .img_bg{
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    filter: blur(10px);
    overflow: hidden;
  }
  .img_show,.img_wrapper{
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%,-50%);
  }
</style>