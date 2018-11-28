<template>
  <div class="modal" @click="closeModal">
    <div class="modal-view" @click.stop>
      <div class="modal-view_title">{{content.title}}</div>
      <div class="modal-view_content">
        <slot name="content"></slot>
      </div>
      <div class="modal-view_btn" @click="closeModal('study')">{{content.btn}}</div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    content: {
      type: Object,
      required: true
    }
  },
  methods: {
    closeModal (type) {
      switch (type) {
        case 'study':
          this.$emit('modalEvent', 'study')
          break
        default:
          this.$emit('modalEvent', 'close')
      }
    }
  }
}
</script>

<style lang="less">
.modal {
  position: fixed;
  left: 0;
  top: 0;
  width: 100vw;
  height: 100vh;
  background-color: rgba(0, 0, 0, 0.5);

  &-view {
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    width: 295px;
    height: 168px;
    background-color: #fff;
    border-radius: 12px;

    &_title {
      margin-top: 30px;
      text-align: center;
      font-size: 18px;
      line-height: 1em;
      // font-weight: bold;
    }

    &_content {
      position: absolute;
      left: 50%;
      transform: translateX(-50%);
      min-width: 90%;
      text-align: center;
      top: 68px;
      line-height: 1em;
    }

    &_btn {
      position: absolute;
      width: 255px;
      height: 40px;
      line-height: 40px;
      bottom: 20px;
      left: 20px;
      text-align: center;
      border-radius: 20px;
      color: #fff;
      background-color: #FF5A31;
      font-weight: bold;
    }
  }
}
</style>
