<template>
  <div class="page3">
    <ul class="content" ref="ul">
      <li v-for="item in swipe" :key="item.id" ref="li" class="swipe_item">
        <img :src="item.src" class="img_bg" :style="height"/>
        <img
          src="https://cyl-blog-1300455867.cos.ap-shanghai.myqcloud.com/travel/img/img_wrapper.7e844ee8.png"
          class="img_wrapper"
        />
        <img :src="item.src" class="img_show" />
      </li>
    </ul>
    <img src='https://cyl-blog-1300455867.cos.ap-shanghai.myqcloud.com/travel/img/arrow_left.f0a0e5ae.png' class="arrow left_arrow" @click="perv"/>
    <img src='https://cyl-blog-1300455867.cos.ap-shanghai.myqcloud.com/travel/img/arrow_right.a119338f.png' class="arrow right_arrow" @click="next"/>
  </div>
</template>



<script>
import BScroll from "better-scroll";
export default {
  name: "thirdPage",
  props: {
    height:{
      type: Object,
      default:{}
    },
    swipe: {
      type: Array,
      default: []
    }
  },
  components: {},
  data() {
    return {
      swipeScroll: null
    };
  },
  mounted() {
    this.swipeScroll = new BScroll(".page3", {
      tap: true,
      probeType: 3,
      scrollX: true,
      scrollY: false,
      bounce: false, // 当滚动超过边缘的时候无回弹动画
      snap: {
        // 滑动切换的一些配置
        speed: 400, // 滑动切换的速度
        loop: true,
        easing: {
          // 滑动切换的动画效果
          style: "ease-in"
        },
        threshold: 0.5, // 滑动切换到超过一半时切换到下一屏
        stepX: window.innerWidth // 横向切换距离为轮播图宽度
      }
    });
    // 动态设置ul的宽度
    this.$refs.ul.style.width = (this.$refs.li.length + 2) * 100 + "vw";
    // this.swipeScroll.on("scrollEnd", () => {
    //   let result = this.swipeScroll.getCurrentPage().pageX;
    //   console.log(result);
    // });
  },
  methods:{
    perv(){
      this.swipeScroll.prev(500,"easing")
    },
    next(){
      this.swipeScroll.next(500,"easing")

    }
  }
};
</script>
<style lang='less' scoped>
.page3 {
  position: relative;
  overflow: hidden;
  .content {
    display: flex;
    .swipe_item {
      position: relative;
      width: 100vw;
      height: 100%;
      .img_bg {
        width: 100%;
        height: 100%;
        filter: blur(10px);
      }
      .img_show {
        position: absolute;
        left: 50%;
        top: 50%;
        transform: translate(-50%, -50%);
        width: 585px;
        height: 860px;
        z-index: 2;
      }
    }
  }
  .img_wrapper {
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    width: 626px;
    height: 1036px;
    z-index: 1;
  }
  .arrow{
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    width: 89px;
    height: 89px;
  }
  .left_arrow{
    left: 38px;
  }
   .right_arrow{
    right: 38px;
  }
}
</style>