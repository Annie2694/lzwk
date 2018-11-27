<template>
  <div class="btn_bar">
    <div class="listen" @click="tryListen">
      <img src="../assets/img/listen.png" class="listenButton"/>试听
    </div>
    <div class="buy">¥99.9购买</div>
  </div>
</template>

<script>
let isClickTryBtn = false

export default {
  data () {
    return {
    }
  },
  methods: {
    tryListen () {
      this.$emit('clickTryBtn', !isClickTryBtn)
    }
  }
}
</script>

<style scoped>
.btn_bar {
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100vw;
  padding: 1vw 4vw;
  display: flex;
  background-color: #fff;
}

.listen {
  width: 50%;
  border: #FF5A31 solid 1px;
  background-color: #FF5A31;
  font-size: 16px;
  color: #FFF;
  letter-spacing: 0;
  text-align: center;
  height: 13.33vw;
  border-bottom-left-radius: 10vw;
  border-top-left-radius: 10vw;
}

.buy {
  width: 50%;
  border: #FF5A31 solid 1px;
  font-size: 16px;
  color: #FF5A31;
  letter-spacing: 0;
  text-align: center;
  height: 13.33vw;
  border-bottom-right-radius: 10vw;
  border-top-right-radius: 10vw;
  padding-top: 4.5vw;
}

.listenButton {
  width: 5.01vw;
  height: 5.01vw;
  margin-right: 1.76vw;
  margin-top: 4.16vw;
}
</style>
