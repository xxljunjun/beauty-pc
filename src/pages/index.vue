<template>
  <div class="home">
    <img src="../assets/building_2.jpg" alt="" class="topimg" />
    <!-- 一 -->
    <div class="top">
      <div class="top-text">
        <div class="tabBar">
          <div class="left">
            <img src="../assets/building.jpg" alt="" class="logo" />
            <div v-for="(item, index) in tabBarArr" :key="index" class="itme">
              {{ item.title }}
            </div>
          </div>
          <div class="right">
            <div class="todemo">View Live Demo</div>
          </div>
        </div>
        <div class="state">
          <p class="txt1">
            Modern Responsive Bootstrap 4 jQuery HTML Dashboard Template
          </p>
          <p class="txt2">
            ArchitectUI comes packed with elements, components and widgets
            nicely bundled together for perfect
            <span>consistency</span
            >,<span>scalability</span>,<span>modularity</span>,
          </p>
        </div>
      </div>
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
    return {
      tabBarArr: [
        { id: 1, title: 'Previews' },
        { id: 2, title: 'Features' },
        { id: 3, title: 'Support' },
        { id: 4, title: 'Buy Now' },
      ],
    }
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
    background: rgba(0, 0, 0, 0.8);
    .top-text {
      width: 1200px;
      height: 650px;
      margin: 0 auto;
      .tabBar {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        height: 110px;
        align-items: center;
        margin-bottom: 100px;
        .left {
          display: flex;
          flex-direction: row;
          justify-content: space-between;
          align-items: center;
          .itme {
            margin-right: 30px;
            color: #fff;
          }
          .logo {
            width: 100px;
            height: 30px;
            margin-right: 60px;
          }
        }
        .right {
          .todemo {
            height: 44px;
            width: 160px;
            background: #f7b924;
            border-radius: 10px;
            border: 2px solid #101f45;
            line-height: 44px;
            text-align: center;
          }
        }
      }
      .state {
        margin: 0 auto;
        text-align: center;
        width: 755px;
        .txt1 {
          color: #fff;
          font-size: 40px;
          line-height: 55px;
          margin-bottom: 25px;
        }
        .txt2 {
          font-size: 22px;
          line-height: 34px;
          color: #b7bfc8;
          span {
            color: #fff;
          }
        }
      }
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