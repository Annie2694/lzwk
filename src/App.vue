<template>
  <div id="app">
    <DetailPage></DetailPage>
    <List></List>
    <Button @clickTryBtn="clickTryBtn"></Button>
    <div class="trial"
         @click="isShowTrialView = false"
         v-if="isShowTrialView"
         @touchmove.prevent
    >
      <div class="trial-view" @click.stop>
        <div class="trial-view__title">听课列表<span class="total">（共10节课）</span></div>
        <div class="class_name free">第1课：脖子挺直挺对，迅速显高5厘米</div>
        <div class="class_name">第2课：拒绝脖子前倾，让自己回归女神气质<img src="./assets/img/secret.png" class="secret_icon"/></div>
        <div class="class_name">第2课：拒绝脖子前倾，让自己回归女神气质<img src="./assets/img/secret.png" class="secret_icon"/></div>
        <div class="class_name">第2课：拒绝脖子前倾，让自己回归女神气质<img src="./assets/img/secret.png" class="secret_icon"/></div>
      </div>
      <audio><source src="./assets/alarm.mp3"/></audio>
      <div class="btn">
        <div class="pauseButton">
          <img src="./assets/img/pause.png" class="pause"/>暂停
        </div>
        <div class="buy1"><div class="buy1-money">仅需支付¥99</div><div class="buy1-now">立即购买</div></div>
      </div>
    </div>
  </div>
</template>

<script>
import DetailPage from '@/components/DetailPage'
import List from '@/components/List'
import Button from '@/components/Button'

export default {
  name: 'App',
  data () {
    return {
      isShowTrialView: false
    }
  },

  components: {
    DetailPage,
    List,
    Button
  },
  methods: {
    clickTryBtn (isShowTrialView) {
      this.isShowTrialView = isShowTrialView
    }
  }
}
</script>

<style lang="less">
body {
  margin: 0;
  background-color: #f8f8f8;
}
div {
  box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
#app {

}

.trial {
  position: fixed;
  width: 100vw;
  height: 100vh;
  background-color: rgba(0, 0, 0, 0.5);
  left: 0;
  top: 0;
  &-view {
    position: absolute;
    width: 100vw;
    bottom: 13.33vw;
    background-color: #fff;
    border-top-left-radius: 10vw;
    border-top-right-radius: 10vw;
    &__title {
      margin-left: 7.7vw;
      margin-top: 8.2vw;
      margin-bottom: 9vw;
      font-size: 18px;
      color: #333333;
      letter-spacing: 0;
      line-height: 18px;
    }
  }
}
.total {
  font-size: 14px;
  color: #999999;
  letter-spacing: 0;
  line-height: 14px;
}
.class_name {
  font-size: 14px;
  color: #999999;
  letter-spacing: 0;
  text-align: justify;
  line-height: 14px;
  margin-left: 5.3vw;
  margin-bottom: 9.6vw;
}
.free {
  color: #333333;
}
.secret_icon {
  width: 4vw;
  height: 4vw;
  margin-left: 11.46vw;
}
.btn {
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100vw;
  display: flex;
  background-color: #fff;
  padding: 1vw 4vw;
}
.pauseButton {
  width: 37%;
  border: #FF5A31 solid 1px;
  font-size: 16px;
  color: #FF5A31;
  letter-spacing: 0;
  text-align: center;
  height: 13.33vw;
  border-bottom-left-radius: 10vw;
  border-top-left-radius: 10vw;
}
.buy1 {
  width: 63%;
  background-color: #FF5A31;
  font-size: 16px;
  color: #fff;
  letter-spacing: 0;
  text-align: center;
  height: 13.33vw;
  border-bottom-right-radius: 10vw;
  border-top-right-radius: 10vw;

  &-money {
    font-size: 12px;
  }
  &-now {
    font-size: 16px;
  }
}
.pause {
  width: 5vw;
  height: 5vw;
}
</style>
