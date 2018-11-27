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
        <div class="class_name">第1课：脖子挺直挺对，迅速显高5厘米</div>
        <div class="class_name">第2课：拒绝脖子前倾，让自己回归女神气质<img src="./assets/img/secret.png" class=""/></div>
        <div class="class_name">第2课：拒绝脖子前倾，让自己回归女神气质</div>
        <div class="class_name">第2课：拒绝脖子前倾，让自己回归女神气质</div>
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
    bottom: 0;
    background-color: #fff;
    border-top-left-radius: 10vw;
    border-top-right-radius: 10vw;
    &__title {
      margin-left: 7.7vw;
      margin-top: 8.2vw;
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
  color: #333333;
  letter-spacing: 0;
  text-align: justify;
  line-height: 14px;
  margin-left: 5.3vw;
  margin-top: 4.8vw;
  margin-bottom: 4.8vw;
}
</style>
