<template>
  <div id="app">
   <mynewmessage class="left"></mynewmessage>
   <mycommunicate class="right"></mycommunicate>
  </div>
</template>

<script>
  import Communicate from './components/Communicate/Communicate.vue'
  import NewMessage from './components/NewMessage/NewMessage.vue'
  export default {
    name: 'app',
    components: {
      mycommunicate: Communicate,
      mynewmessage: NewMessage
    }
  }
</script>

<style lang="less">
  body{
    background-color: #F4EDD7;
    #app {
      height: 700px;
      width: 950px;
      margin: 50px auto;
      background-color: white;
    .left {
      float: left;
      margin: 0 25px;
    }
    .right {
      float: left;
      margin-right: 50px;
    }
    }
    }

</style>
