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
    this.scroll = new BScroll(".wrapper")
  },
};
</script>
<style lang='less' scoped>
</style>