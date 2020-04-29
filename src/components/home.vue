<template>
  <div class="home">
    <scroll class="scroll">
      <div class="page1"></div>
      <div class="page2">
        <img src="../assets/img/page2_bg.png" alt="" class="page2_bg">
        <div class="page2_content">
          <div class="page2_img">
            <img src="../assets/img/page2_img.png" alt="">
          </div>
          <div class="audio">
            <audio src="163.com" controls></audio>
          </div>
          <div class="view_spot">
            <scroll class="scroll_sub">
              <span>XX风景区，位于江苏省常熟市南隅，属阳澄湖水系，周边水网密布，交通便利，现为国家5A级景区、国家湿地公园、全国百家红色旅游经典景区。沙家浜风景区拥有独特的历史人文和自然生态资源，目前形成革命传统教育区、红石民俗文化村、芦苇水陆迷宫、国防教育园、横泾老街影视基地、拥有优质的旅游资源与丰富的体验项目。XX风景区，位于江苏省常熟市南隅，属阳澄湖水系，周边水网密布，交通便利，现为国家5A级景区、国家湿地公园、全国百家红色旅游经典景区。沙家浜风景区拥有独特的历史人文和自然生态资源，目前形成革命传统教育区、红石民俗文化村、芦苇水陆迷宫、国防教育园、横泾老街影视基地、拥有优质的旅游资源与丰富的体验项目。</span>
            </scroll>
          </div>
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
     background: url('../assets/img/page1_bg.jpg') no-repeat center/cover
    }
    .page2{
      .box-size();
      position: relative;
      .page2_bg{
        .box-size();
        filter: blur(3px);
      }
      .page2_content{
        .box-size();
        position: absolute;
        left: 0;
        top: 0;
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
        align-items: center;
      }
      .page2_img,.view_spot{
       width: 650/2px;
      }
      .scroll_sub{
        height: 300/2px;
        overflow: hidden;
      }
      .view_spot{
        text-align: justify;
        line-height: 2;
      }
    }
  }
</style>