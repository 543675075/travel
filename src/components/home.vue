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
              <span>XX风景区，位于江苏省常熟市南隅，属阳澄湖水系，周边水网密布，交通便利，现为国家5A级景区、国家湿地公园、全国百家红色旅游经典景区。沙家浜风景区拥有独特的历史人文和自然生态资源，目前形成革命传统教育区、红石民俗文化村、芦苇水陆迷宫、国防教育园、横泾老街影视基地、拥有优质的旅游资源与丰富的体验项目。</span>
            </scroll>
          </div>
        </div>
      </div>
      <div class="page3">
        <swipe :swipe="swipe"></swipe>
      </div>
    </scroll>
  </div>
</template>



<script>
import Scroll from "../components/commen/bs";
import Swipe from '../components/commen/swipe'
export default {
  name: "Home",
  components: {
    Scroll,
    Swipe
  },
  data() {
    return {
      swipe:[
        {
          id: 1,
          src: require('@/assets/img/page3_swipe1.png')
        },
        {
        id: 2,
        src: require('@/assets/img/page3_swipe1.png')
        },
        {
        id: 3,
        src: require('@/assets/img/page3_swipe1.png')
        },
      ]
    };
  }
};
</script>
<style lang='less' scoped>
  .box_size(){
      width: 100vw;
      height: 100vh;
  }
  .scroll{
   .box_size();
    overflow: hidden;
    .page1{
     .box_size();
     background: url('../assets/img/page1_bg.jpg') no-repeat center/cover
    }
    .page2{
      .box_size();
      position: relative;
      .page2_bg{
        .box_size();
        filter: blur(3px);
      }
      .page2_content{
        .box_size();
        position: absolute;
        left: 0;
        top: 0;
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
        align-items: center;
        audio{
          width: 650px;
        }
      }
      .page2_img img{
       width: 650px;
      }
      .scroll_sub{
        height: 300px;
        // background: #ccc;
        overflow: hidden;
      }
      .view_spot{
        width: 650px;
        text-align: justify;
        line-height: 2;
      }
    }
    .page3{
      .box_size()
    }
  }
</style>