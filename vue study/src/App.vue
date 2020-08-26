<template>
  <div id="app">
    <p>{{ message }}</p>
    <button v-on:click="reverseMessage">反转消息</button><br><br><br><br>
    <span>parentmsg:{{parentmsg}}</span>
    <router-view :parentmsg="parentmsg" @childmsg="updateChild" />
  </div>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      parentmsg: '11111',
      message: 'Hello Vue.js!'
    }
  },
  methods: {
    updateChild (e) {
      this.childmsg = e
      console.log(this.childmsg)
    },
    reverseMessage: function () {
      console.log(this.message)
      this.message = this.message.split('').reverse().join('')
      console.log(this.message)
    }
  }
}
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
