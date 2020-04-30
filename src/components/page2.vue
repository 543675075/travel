<template>
  <div class="page2">
    <img
      src="https://cyl-blog-1300455867.cos.ap-shanghai.myqcloud.com/travel/img/page2_img.0fa37197.png"
      class="img_show"
    />
    <audio src="163.com" controls></audio>
    <span
      class="text"
    >XX风景区，位于江苏省常熟市南隅，属阳澄湖水系，周边水网密布，交通便利，现为国家5A级景区、国家湿地公园、全国百家红色旅游经典景区。沙家浜风景区拥有独特的历史人文和自然生态资源，目前形成革命传统教育区、红石民俗文化村、芦苇水陆迷宫、国防教育园、横泾老街影视基地、拥有优质的旅游资源与丰富的体验项目。</span>
  </div>
</template>



<script>
export default {
  name: "secondPage",
  components: {},
  data() {
    return {};
  }
};
</script>
<style lang='less' scoped>
.page2 {
  display: flex;
  flex-direction: column;
  align-items: center;
  background: url(https://cyl-blog-1300455867.cos.ap-shanghai.myqcloud.com/travel/img/page2_bg.38eab5bd.png)
    no-repeat center/cover;
  .img_show {
    margin-top: 97px;
    width: 650px;
    height: 669px;
  }
  audio {
    width: 650px;
    height: 60px;
    margin: 69px 0 50px 0;
  }
  .text {
    display: block;
    width: 650px;
    text-align: justify;
    font-size: 24px;
    line-height: 50px;
  }
}
</style>