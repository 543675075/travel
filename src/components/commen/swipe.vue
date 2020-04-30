<template>
  <div class="swipe">
    <img src="https://cyl-blog-1300455867.cos.ap-shanghai.myqcloud.com/travel/img/arrow_left.f0a0e5ae.png" class="arrow arrow_left" />
    <img src="https://cyl-blog-1300455867.cos.ap-shanghai.myqcloud.com/travel/img/arrow_right.a119338f.png" class="arrow arrow_right" />
    <van-swipe class="my_swipe" autoplay="false" indicator-color="white" :show-indicators="false">
    <img src="https://cyl-blog-1300455867.cos.ap-shanghai.myqcloud.com/travel/img/img_wrapper.7e844ee8.png" class="img_wrapper" />
      <van-swipe-item v-for="item in swipe" :key="item.id">
        <img :src="item.src" class="img_bg" />
        <img :src="item.src" class="img_show" />
      </van-swipe-item>
    </van-swipe>
  </div>
  
</template>



<script>
export default {
  name: "Swipe",
  props: {
    swipe: {
      type: Array,
      default: []
    }
  }
};
</script>
<style lang='less' scoped>
.swipe {
  position: relative;
  .arrow {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    width: 85px;
    height: 85px;
    z-index: 999;
  }
  .arrow_left {
    left: 40px;
  }
  .arrow_right {
    right: 40px;
  }
}
.my_swipe{
  // position: relative;
  // background: url('https://cyl-blog-1300455867.cos.ap-shanghai.myqcloud.com/travel/img/img_wrapper.7e844ee8.png') no-repeat top left;
}
.my_swipe .van-swipe-item {
  position: relative;
  width: 100vw;
  height: 100vh;
}
.img_bg {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  filter: blur(10px);
  overflow: hidden;
}
.img_show,
.img_wrapper {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}
.img_show {
  width: 586px;
  height: 852px;
  z-index: 3;
}
.img_wrapper {
  width: 626px;
  height: 1036px;
  z-index: 2;
}
</style>