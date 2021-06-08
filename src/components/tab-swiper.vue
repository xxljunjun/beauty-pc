<template>
  <div class="tab-swiper">
    <div class="first">
      <img src="../../statics/building.jpg" alt="" class="smalllogo" />
      <p class="text_1">Technical Support</p>
      <p class="text_2">
        Get in touch with us if you require assistance. We want to help you
        build wonderful apps!
      </p>
    </div>
    <div class="tabBars">
      <div
        :class="whoItem == item ? 'clickitem old' : 'old'"
        v-for="(item, index) in 4"
        :key="index"
        @click="chooseitem(item)"
      >
        Components
      </div>
    </div>
    <div class="clickConetent1" v-if="whoItem == 1">
      <div class="txt">
        <div class="margintxt">
          <div class="txt-inner" v-for="(item, index) in 9" :key="index">
            <p class="titles">Elements</p>
            <p class="txts">
              There are over 50 unique elements included, that can be bundled
              together to create even more variations.
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="clickConetent2" v-else-if="whoItem == 2">22222222222</div>
    <div class="clickConetent3" v-else-if="whoItem == 3">333333333333</div>
    <div class="clickConetent4" v-else-if="whoItem == 4">4444444444</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      whoItem: 1,
    }
  },
  methods: {
    chooseitem(item) {
      console.log('111111111', item)
      this.whoItem = item
    },
  },
}
</script>

<style lang="scss" scoped>
.tab-swiper {
  .first {
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
      color: #8d99a4;
      font-size: 18px;
      margin-bottom: 35px;
    }
  }
  .tabBars {
    margin: 0 auto;
    width: 1200px;
    height: 80px;
    border-radius: 40px;
    box-sizing: border-box;
    border: 2px solid #eee;
    display: flex;
    align-items: center;
    justify-content: space-around;
    margin-bottom: 35px;
    .old {
      cursor: pointer;
      height: 50px;
      padding: 0 90px;
      border-radius: 25px;
      line-height: 50px;
    }
    .clickitem {
      background: #3f6ad8;
    }
  }
  .clickConetent1 {
    .txt {
      height: 550px;
      width: 100%;
      background: #fff;
      border-top: 4px solid #f7f7f8;
      .margintxt {
        width: 1200px;
        margin: 0 auto;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        align-items: center;
        .txt-inner {
          text-align: center;
          width: 360px;
          margin-top: 60px;
          .titles {
            font-size: 18px;
            color: #000;
          }
          .txts {
          }
        }
      }
    }
  }
}
</style>