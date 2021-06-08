<template>
  <div class="home">
    <img src="../assets/building_2.jpg" alt="" class="topimg" />
    <!-- 一 -->
    <div class="top">
      <div class="top-text"></div>
    </div>
    <!-- 二 -->
    <div class="content"></div>
    <!-- 三 -->
    <div class="box"></div>
    <!-- 四 -->
    <div class="tab">
      <TabSwiper />
    </div>
    <!-- 五 -->
    <div class="txt"></div>
    <!-- 六 -->
    <div class="bottom"></div>
    <!-- 七 -->
    <div class="last"></div>
  </div>
</template>

<script>
import TabSwiper from '@/components/tab-swiper.vue'
export default {
  components: {
    TabSwiper,
  },
  data() {
    return {}
  },
  methods: {},
}
</script>

<style lang="scss" scoped>
.home {
  width: 100%;
  height: 100%;
  .topimg {
    position: fixed;
    width: 100%;
    z-index: -1;
    height: 1080px;
    top: 0;
  }
  .top {
    width: 100%;
    height: 650px;
    background: rgba(0, 0, 0, 0.7);
    .top-text {
      width: 1200px;
      height: 650px;
      margin: 0 auto;
    }
  }
  .content {
    width: 100%;
    height: 1190px;
    background: #fff;
    margin: 0 auto;
  }
  .box {
    width: 100%;
    height: 425px;
    background: #f8f9fa;
  }
  .tab {
    width: 100%;
    height: 1480px;
    background: #fff;
  }
  .txt {
    height: 550px;
    width: 100%;
    background: #fff;
    border-top: 4px solid #f7f7f8;
  }
  .bottom {
    width: 100%;
    height: 430px;
    background: rgba(0, 0, 0, 0.7);
  }
  .last {
    height: 130px;
    width: 100%;
    background: #f1f4f6;
  }
}
</style>