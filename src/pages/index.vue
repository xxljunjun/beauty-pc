<template>
  <div class="home">
    <img src="../..//statics/building_2.jpg" alt="" class="topimg" />
    <!-- 一 -->
    <div class="top">
      <div class="top-text">
        <div class="tabBar">
          <div class="left">
            <img src="../../statics/building.jpg" alt="" class="logo" />
            <div v-for="(item, index) in tabBarArr" :key="index" class="item">
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
    <div class="content">
      <div class="content-inner">
        <p class="blue-txt">jQuery Bootstrap 4 HTML Version</p>
        <p class="black-txt">
          Use with whatever server side language you prefer. Plain HTML, powered
          by jQuery, HTML, Bootstrap 4 and Webpack (used for compiling SCSS and
          JS).
        </p>
        <div class="header-title">Dashboards Demos</div>
        <div class="demo-box">
          <div class="img-box" v-for="(item, index) in demoArr" :key="index">
            <div class="who">
              <img :src="item.path" alt="0" class="demoimg" />
              <div class="img-overly">view demo</div>
            </div>
          </div>
        </div>
        <div class="demo-bottom">
          <div class="txt-box" v-for="(item, index) in 2" :key="index">
            <h4>10 Different Dashboards Available</h4>
            <p>
              Architect comes packed with over 8 different types of dashboards -
              ready to use. If you get stuck, we're here to help.
            </p>
          </div>
        </div>
      </div>
    </div>
    <!-- 三 -->
    <div class="box">
      <img src="../../statics/building.jpg" alt="" class="smalllogo" />
      <p class="text_1">Technical Support</p>
      <p class="text_2">
        Get in touch with us if you require assistance. We want to help you
        build wonderful apps!
      </p>
      <p class="text_3">
        The documentation files can be found inside the template package folder.
      </p>
      <div class="line"></div>
      <div class="btn">Send us an email</div>
    </div>
    <!-- 四 -->
    <div class="tab">
      <TabSwiper />
    </div>
    <!-- 六 -->
    <div class="bottom">
      <img src="../../statics/building.jpg" alt="" class="smalllogo" />
      <p class="text_1">Purchase Architect UI Dashboard Template</p>
      <p class="text_2">
        You're making the smart choice. Enjoy a well built Bootstrap 4 Admin
        Template built for jQuery/HTML!
      </p>
      <div class="btn">
        <img src="../../statics/building.jpg" alt="" class="shop" />
        <div>Buy on DashboardPack</div>
      </div>
    </div>
    <!-- 七 -->
    <div class="last">
      <p>Copyright © 2021 ArchitectUI</p>
    </div>
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
      demoArr: [
        { id: 1, path: require('../../statics/building.jpg') },
        { id: 2, path: require('../../statics/building.jpg') },
        { id: 3, path: require('../../statics/building.jpg') },
        { id: 4, path: require('../../statics/building.jpg') },
        { id: 5, path: require('../../statics/building.jpg') },
        { id: 6, path: require('../../statics/building.jpg') },
        { id: 7, path: require('../../statics/building.jpg') },
        { id: 8, path: require('../../statics/building.jpg') },
        { id: 9, path: require('../../statics/building.jpg') },
      ],
    }
  },
  mounted() {},
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
          .item {
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
    .content-inner {
      width: 1200px;
      height: 1190px;
      background: #fff;
      margin: 0 auto;
      position: relative;
      top: -110px;
      border-radius: 8px;
      display: flex;
      flex-direction: column;
      align-items: center;
      .blue-txt {
        margin: 35px 0 14px;
        color: #0026c4;
        font-size: 18px;
      }
      .black-txt {
        font-size: 14px;
        color: #000;
      }
      .header-title {
        margin: 80px 0 40px;
        font-size: 18px;
        color: #000;
      }
      .demo-box {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        flex-wrap: wrap;
        margin-bottom: 30px;
        padding: 0 40px;
        .img-box {
          width: 320px;
          height: 270px;
          border-radius: 8px;
          margin-bottom: 32px;
          box-sizing: border-box;
          box-shadow: 0px 10px 24px 2px #848484;
          cursor: pointer;
          background: #000;
          .who {
            position: relative;
            &:hover .demoimg {
              border-radius: 50px;
              transform: scale(1.2);
            }
            &:hover .img-overly {
              opacity: 1;
              transform: scale(1.2);
              border-radius: 50px;
            }
            .demoimg {
              width: 320px;
              height: 270px;
              border-radius: 8px;
              transition: 0.3s;
            }
            .img-overly {
              position: absolute;
              opacity: 0;
              width: 100%;
              height: 100%;
              background: rgba(0, 0, 0, 0.5);
              transition: all 0.2s;
              z-index: 6;
              left: 0;
              top: 0;
              color: #fff;
              text-align: center;
              display: flex;
              flex-direction: column;
              justify-content: center;
            }
          }
        }
      }
      .demo-bottom {
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: space-between;
        .txt-box {
          width: 580px;
          height: 110px;
          border: 2px solid #f2f4f8;
          text-align: center;
          padding: 0 20px;
          box-sizing: border-box;
          border-radius: 6px;
          h4 {
            font-weight: normal;
            color: #000;
            margin: 15px 0;
            font-size: 18px;
          }
          p {
            color: #49545f;
          }
        }
      }
    }
  }
  .box {
    width: 100%;
    height: 425px;
    background: #f8f9fa;
    display: flex;
    flex-direction: column;
    align-items: center;
    .smalllogo {
      width: 60px;
      height: 60px;
      border-radius: 50%;
      margin: 60px 0 25px;
    }
    .text_1 {
      color: #000;
      font-size: 22px;
      margin-bottom: 16px;
    }
    .text_2 {
      color: #2c2c2c;
      font-size: 18px;
      margin-bottom: 16px;
    }
    .text_3 {
      color: #033ace;
      font-size: 22px;
      margin-bottom: 55px;
    }
    .line {
      height: 2px;
      width: 1200px;
      background: #eaedf0;
    }
    .btn {
      width: 220px;
      height: 50px;
      background: #28b0cd;
      border-radius: 10px;
      margin-top: 26px;
      line-height: 50px;
      text-align: center;
      color: #fff;
      font-size: 18px;
    }
  }
  .tab {
    width: 100%;
    height: 1480px;
    background: #fff;
  }
  .bottom {
    width: 100%;
    height: 430px;
    background: rgba(0, 0, 0, 0.7);
    display: flex;
    flex-direction: column;
    align-items: center;
    .smalllogo {
      width: 60px;
      height: 60px;
      border-radius: 50%;
      margin: 60px 0 25px;
    }
    .text_1 {
      color: #fff;
      font-size: 22px;
      margin-bottom: 16px;
    }
    .text_2 {
      color: #c2ccd6;
      width: 750px;
      font-size: 18px;
      margin-bottom: 16px;
      text-align: center;
      line-height: 26px;
    }
    .btn {
      width: 345px;
      height: 80px;
      background: #3ac47d;
      border-radius: 10px;
      margin-top: 26px;
      text-align: center;
      color: #fff;
      font-size: 18px;
      display: flex;
      align-items: center;
      justify-content: center;
      .shop {
        height: 24px;
        width: 24px;
        margin-right: 15px;
      }
    }
  }
  .last {
    height: 130px;
    width: 100%;
    background: #f1f4f6;
    p {
      text-align: center;
      padding-top: 55px;
    }
  }
}
</style>