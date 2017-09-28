<template>
  <div class="bigbox">
    <h2 class="missMessage">
      单前未读消息:1
    </h2>
    <div class="missMessageList" ref="messageList">
      <div class="box">
        <div :class="{smallbox: ok, highlight: isHighlight}" @click.once="change">
          <div class="message message2">
            <div class="title">
              <h3 class="name">BILL</h3>
              <p class="time">15286245445588445</p>
            </div>
            <div class="content content2">价格可垃圾速度快挂机啊快点睡觉dgfdgagfdggdfga</div>
          </div>
        </div>
        <div :class="{smallbox: ok, highlight: isHighlight}" @click.once="change">
          <div class="message message2">
            <div class="title">
              <h3 class="name">BILL</h3>
              <p class="time">15286245445588445</p>
            </div>
            <div class="content content2">价格可垃圾速度快挂机啊快点睡觉dgfdgagfdggdfga</div>
          </div>
        </div>
        <div :class="{smallbox: ok, highlight: isHighlight}" @click.once="change">
          <div class="message message2">
            <div class="title">
              <h3 class="name">BILL</h3>
              <p class="time">15286245445588445</p>
            </div>
            <div class="content content2">价格可垃圾速度快挂机啊快点睡觉dgfdgagfdggdfga</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import IScroll from 'iscroll/build/iscroll-probe'
  export default {
    data () {
      return {
        isHighlight: true,
        ok: true
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
      },
      change () {
        this.isHighlight = false
      }
    }
  }
</script>

<style lang="less" scoped>
  @import "../../common/basic.less";
  @import "../../common/main.less";
  .bigbox {
    width: 250px;
    height: 700px;
    .missMessage {
      font-size: 25px;
      height: 50px;
      margin: 0;
    }
    .missMessageList {
      width: 100%;
      height: 450px;
      border: 1px solid mediumpurple;
      box-sizing: border-box;
      overflow: hidden;
      .smallbox {
        border-bottom: 1px solid mediumpurple;
        .message2 {
          padding: 0 15px;
        }
      }
     .highlight {
       background: #F0D4FF;
     }
    }
  }
</style>
