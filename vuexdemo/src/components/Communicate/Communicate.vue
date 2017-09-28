<template>
  <div class="bigbox">
    <h1 class="titlename">群名</h1>
    <div class="messageList" ref="messageList">
      <div class="box">
        <div class="message">
          <div class="title">
            <h3 class="name">BILL</h3>
            <p class="time">15286245445588445</p>
          </div>
          <div class="content">价格可垃圾速度快挂机啊快点睡觉</div>
        </div>
      </div>
    </div>
    <textarea class="text"></textarea>
    <button class="send">send</button>
  </div>
</template>

<script>
  import IScroll from 'iscroll/build/iscroll-probe'
  export default {
    data () {
      return {
        message: ''
      }
    },
    created () {
      this.$nextTick(() => {
        this.initScrollTemplate()
      })
    },
    methods: {
      initScrollTemplate () {
        if (this.$refs.messageList) {
          this.messageScroll = new IScroll(this.$refs.messageList, {
            click: true,
            mouseWheel: true
          })
        }
      }
    }

  }
</script>

<style lang="less" scoped>
  @import "../../common/basic.less";
  @import "../../common/main.less";

  .bigbox {
    width: 600px;
    height: 700px;
    .titlename {
      font-size: 25px;
      font-weight: 800;
      height: 50px;
      margin: 0;
    }
  .messageList {
    width: 100%;
    height: 450px;
    border: 1px solid mediumpurple;
    box-sizing: border-box;
    font-size: 20px;
    padding: 0 15px;
    overflow: hidden;
  }
    .text {
      width: 100%;
      height: 120px;
      margin: 20px 0 5px;
    }
    .send {
      display: block;
      border: none;
      background-color: @black;
      color: white;
      padding: 5px;
      border-radius: 5px;
      float: right;
    }
  }
</style>
