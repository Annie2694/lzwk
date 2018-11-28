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
        <div class="handle" @click="isShowTrialView=false"></div>
        <div class="trial-view__title"><div class="nuu"></div>听课列表<div class="total">（共10节课）</div></div>
        <div class="class_name free">第1课：脖子挺直挺对，迅速显高5厘米</div>
        <div class="class_name" @click="isShowModal=true">第2课：拒绝脖子前倾，让自己回归女神气质<img src="./assets/img/secret.png" class="secret_icon"/></div>
        <div class="class_name" @click="isShowModal=true">第2课：拒绝脖子前倾，让自己回归女神气质<img src="./assets/img/secret.png" class="secret_icon"/></div>
        <div class="class_name" @click="isShowModal=true">第2课：拒绝脖子前倾，让自己回归女神气质<img src="./assets/img/secret.png" class="secret_icon"/></div>
      </div>
      <input type="range" value="0" class="slideBar">
      <div class="btn" @click.stop>
        <div class="pauseButton" @click="isShowTrialView = false">
          <img src="./assets/img/pause.png" class="pause"/>暂停
        </div>
        <div class="buy1"><div class="buy1-money">仅需支付¥99</div><div class="buy1-now">立即购买</div></div>
      </div>
    </div>
    <Modal :content="modalContent" v-if="isShowModal" @modalEvent="getModal">
      <div slot="content" style="color:#666">
        点击<font color="#FF5A31">下方按钮</font>即可学习所有课程
      </div>
    </Modal>
  </div>
</template>

<script>
import DetailPage from '@/components/DetailPage'
import List from '@/components/List'
import Button from '@/components/Button'
import Modal from '@/components/Modal'

export default {
  name: 'App',
  data () {
    return {
      isShowTrialView: false,
      isShowModal: false,
      modalContent: {
        title: '你还未购买该专栏',
        btn: '我要学习'
      }
    }
  },

  components: {
    DetailPage,
    List,
    Button,
    Modal
  },
  methods: {
    clickTryBtn (isShowTrialView) {
      this.isShowTrialView = isShowTrialView
    },
    getModal (type) {
      switch (type) {
        case 'study':
          this.isShowModal = false
          break
        case 'close':
          this.isShowModal = false
          break
      }
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
    bottom: 15.2vw;
    background-color: #fff;
    border-top-left-radius: 10vw;
    border-top-right-radius: 10vw;
    &__title {
      margin-left: 5.3vw;
      margin-top: 4.26vw;
      margin-bottom: 9vw;
      font-size: 18px;
      color: #333333;
      letter-spacing: 0;
      line-height: 18px;
      display: flex;
    }
  }
}
.total {
  font-size: 14px;
  color: #999999;
  letter-spacing: 0;
  line-height: 14px;
  margin-top: 1vw;
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
  padding-top: 3vw;
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
  padding-top: 1.5vw;
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
  margin-right: 1vw;
  position: relative;
  bottom: -1vw;
}
.nuu {
  background-color: #FF5A31;
  border: solid 2px #FF5A31;
  margin-right: 5px;
  height: 4.8vw;
}
.handle {
  width: 10.6vw;
  border: solid 2px #999999;
  margin-left: 44.8vw;
  margin-top: 2.9vw;
}
.slideBar {
  width: 80vw;
  position: fixed;
  bottom: 16vw;
  left: 8vw;
}
</style>
