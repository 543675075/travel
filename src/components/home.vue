<template>
  <div class="home">
    <scroll class="scroll">
      <div class="page1"></div>
      <div class="page2">
        <img src="../assets/img/page2_bg.png" alt="" class="page2_bg">
        <div class="page2_img">
          <img src="../assets/img/page2_img.png" alt="">
        </div>
        <div class="audio">
          <audio src="163.com" controls></audio>
        </div>
      </div>
    </scroll>
  </div>
</template>



<script>
import Scroll from "../components/commen/bs";
export default {
  name: "Home",
  components: {
    Scroll
  },
  data() {
    return {};
  }
};
</script>
<style lang='less' scoped>
  .box-size(){
      width: 100vw;
      height: 100vh;
  }
  .scroll{
   .box-size();
    overflow: hidden;
    .page1{
     .box-size();
     background: url('../assets/img/page1_bg.jpg')
    }
    .page2{
      .box-size();
      position: relative;
      .page2_bg{
        filter: blur(3px);
      }
      .page2_img{
        position: absolute;
        left: 50%;
        top: 97/2px;
        transform: translateX(-50%);
      }
    }
  }
</style>