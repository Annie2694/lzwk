<template>
  <div class="button">
    <div class="listen" @click="start()">
      <img src="../assets/img/listen.png" class="listenButton"/>试听
    </div>
    <div class="buy">¥99.9购买</div>
  </div>
</template>

<script>
export default {
  methods: {
    start() {

    }
  }
}
</script>

<style scoped>
.button {
  display: flex;
  background-color: #fff;
}

.listen {
  width: 45.8vw;
  border: #FF5A31 solid 1px;
  background-color: #FF5A31;
  font-size: 16px;
  color: #FFF;
  letter-spacing: 0;
  text-align: center;
  line-height: 16px;
  margin-left: 4vw;
  height: 13.33vw;
  border-bottom-left-radius: 50px;
  border-top-left-radius: 50px;
}

.buy {
  width: 46.1vw;
  border: #FF5A31 solid 1px;
  font-size: 16px;
  color: #FF5A31;
  letter-spacing: 0;
  text-align: center;
  line-height: 16px;
  height: 13.33vw;
  border-bottom-right-radius: 50px;
  border-top-right-radius: 50px;
  padding-top: 4.5vw;
}

.listenButton {
  width: 5.01vw;
  height: 5.01vw;
  margin-right: 1.76vw;
  margin-top: 4.16vw;
}
</style>
