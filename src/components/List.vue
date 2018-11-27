<template>
  <div class="list">
    <div class="tag">
      <div class="tag1">课程介绍</div>
      <div class="tag2">听课列表</div>
    </div>
    <div class="lessons">
      <div class="lesson">
        <div class="lesson-title">
          <div class="name">第1课 目标选择：找对方向是一切努力的根基</div>
          <div class="time"><img src="../assets/img/time.png" class="clock"/>28分钟</div>
        </div>
        <img src="../assets/img/cover.png" class="cover"/>
      </div>
      <div class="lesson">
        <div class="lesson-title">
          <div class="name">第1课 目标选择：找对方向是一切努力的根基</div>
          <div class="time"><img src="../assets/img/time.png" class="clock"/>12-08 14:00</div>
        </div>
        <img src="../assets/img/cover.png" class="cover"/>
      </div>
      <div class="lesson">
        <div class="lesson-title">
          <div class="name">第1课 目标选择：找对方向是一切努力的根基</div>
          <div class="time"><img src="../assets/img/secret.png" class="clock"/>加密课</div>
        </div>
        <img src="../assets/img/cover.png" class="cover"/>
      </div>
      <div class="lesson">
        <div class="lesson-title">
          <div class="name">第1课 目标选择：找对方向是一切
            努力的根基</div>
          <div class="time orange"><img src="../assets/img/free.png" class="clock"/>免费试听</div>
        </div>
        <img src="../assets/img/cover.png" class="cover"/>
      </div>
      <div class="lesson">
        <div class="lesson-title">
          <div class="name"><img src="../assets/img/video.png" class="video"/>第1课 目标选择：找对方向是一切努力的根基</div>
          <div class="time"><img src="../assets/img/time.png" class="clock"/>正在排课</div>
        </div>
        <img src="../assets/img/cover.png" class="cover"/>
      </div>
    </div>
  </div>
</template>

<script>


</script>

<style scoped>
.tag {
  display: flex;
  background-color: #fff;
  height: 12.27vw;
  width: 100vw;
}

.tag1 {
  flex: 1;
  width: 50vw;
  text-align: center;
  font-size: 14px;
  color: #999999;
  margin-top: 3.5vw;
}

.tag2 {
  width: 50vw;
  text-align: center;
  font-size: 14px;
  margin-top: 3.5vw;
}

.lessons {
  background-color: #fff;
  width: 100vw;
  padding-top: 2.6vw;
  padding-bottom: 2.6vw;
}

.lesson-title {

}

.lesson {
  background-color: #f8f8f8;
  width: 94.67vw;
  height: 26.67vw;
  margin-left: 2.6vw;
  margin-bottom: 2.6vw;
  border-radius: 5px;
  display: flex;
}

.cover {
  width: 32vw;
  height: 18.56vw;
  border-radius: 3px;
  margin-left: 2.6vw;
  margin-top: 4vw;
}

.name {
  width: 52vw;
  font-size: 14px;
  color: #333333;
  letter-spacing: 0;
  text-align: justify;
  line-height: 18px;
  margin-left: 4vw;
  margin-top: 4vw;
  margin-bottom: 5.8vw;
}

.time {
  font-size: 12px;
  color: #999999;
  letter-spacing: 0;
  text-align: left;
  margin-left: 4.2vw;
}

.video {
  width: 6.67vw;
  height: 3.73vw;
  margin-right: 1.33vw;
}

.clock {
  width: 2.67vw;
  height: 2.64vw;
  margin-right: 1.33vw;
}

.orange {
  color: #FF5A31;
}
</style>
