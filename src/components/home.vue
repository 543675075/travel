<template>
  <div class="home" >
    <scroll class="scroll" :style="height">
      <first-page class="page" :style="height" />
      <second-page class="page" :style="height" />
      <third-page class="page" :swipe="swipe" :style="height" :height="height"/>
    </scroll>
  </div>
</template>



<script>
import Scroll from "../components/commen/bs";
import firstPage from './page1'
import secondPage from './page2'
import thirdPage from './page3'
export default {
  name: "Home",
  components: {
    Scroll,
    firstPage,
    secondPage,
    thirdPage
  },
  
  data() {
    return {
      height: {
        height: ''
      },
      swipe:[
        {
          id: 1,
          src: 'https://cyl-blog-1300455867.cos.ap-shanghai.myqcloud.com/travel/img/page3_swipe1.ca8a61c4.png'
        },
        {
        id: 2,
        src: 'https://cyl-blog-1300455867.cos.ap-shanghai.myqcloud.com/travel/img/page1_bg.97059e79.jpg'
        },
        {
          id: 3,
          src: 'https://cyl-blog-1300455867.cos.ap-shanghai.myqcloud.com/travel/img/page3_swipe1.ca8a61c4.png'
        },
      ]
    };
  },
  mounted(){
    this.getHeight()
  },
  methods:{
    // 获取浏览器的实际高度
    getHeight(){
      this.height.height = window.innerHeight+'px'
    }
  }
};
</script>
<style lang='less' scoped>
  .scroll{
    width: 100vw;
    overflow: hidden;
  }
</style>