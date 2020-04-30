<template>
  <div class="wrapper">
    <div class="content">
      <slot></slot>
    </div>
  </div>
</template>



<script>
import BScroll from "better-scroll";

export default {
  name: "Scroll",
  components: {},
  data() {
    return {
      scroll: null
    };
  },
  mounted() {
    this.scroll = new BScroll(".wrapper", {
      click: true,
      stopPropagation: true,
      snap: {
        // 滑块切换的一些配置
        threshold: 0.5, // 滑动切换到超过一半时切换到下一屏
        stepY: window.innerHeight // 纵向切换距离为窗口高度
      }
    });
  }
};
</script>
<style lang='less' scoped>
</style>