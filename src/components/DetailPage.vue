<template>
  <div class="container">
    <!--<div class="container-poster" :style="`background: url('${bgImg}')`">-->
    <div class="container-poster" :style="'background-image: url(' + bgImg + ');'">
      <div class="container-poster__subtitle">
        <img src="../assets/img/right_icon.png">
        <div class="container-poster__subtitle-text">{{count}}万次学习</div>
        <div class="container-poster__subtitle-tag">永久回听</div>
      </div>
    </div>
    <div class="container-header">
      <div class="container-header__title">{{title}}</div>
      <div class="container-header__subtitle">{{subtitle}}</div>
      <div class="container-header__subtitle">已更新31节/共40节</div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      count: 5.4,
      bgImg: 'http://d.ifengimg.com/w600/p0.ifengimg.com/pmop/2018/0531/AA1AD3CC878DEAF9CD7540E41B0DC26FAB937367A_size62_w840_h480.jpeg',
      title: '超级演说家刘媛媛：普通人必备的实用逆袭法，带你实现颠覆性改变',
      subtitle: '没资源没人脉不拼爹，普通人如何绝地反击？教你抓机会、定方向、找跳板、逆袭的底层逻辑！'
    }
  }
}
</script>

<style scoped lang="less">
.container {
  width: 100vw;

  &-poster {
    width: 100vw;
    height: 56.53vw;
    background-size: cover;
    -webkit-background-size: cover;
    position: relative;

    &__subtitle {
      position: absolute;
      bottom: 0;
      width: 100%;
      height: 40px;
      display: flex;
      align-items: center;
      color: #fff;
      background-color: rgba(0, 0, 0, 0.5);
      font-size: 12px;

      > img {
        width: 14px;
        height: 14px;
        margin-left: 15px;
      }

      &-text {
        margin-left: 5px;
        line-height: 14px;
        height: 14px;
        flex: 1;
      }

      &-tag {
        margin-right: 4vw;
        padding: 5px;
        background-color: rgba(255, 255, 255, 0.2);
        border-radius: 5px;
      }
    }
  }

  &-header {
    width: 100%;
    padding: 4vw;
    margin-bottom: 2.57vw;
    background: #fff;

    &__title {
      font-weight: bold;
      font-size: 18px;
      color: #333333;
      margin-bottom: 2.57vw;
    }

    &__subtitle {
      font-size: 12px;
      color: #999999;
      text-align: justify;
      line-height: 16px;

      &:last-child {
        margin-top: 2.57vw;
      }
    }
  }
}
</style>
