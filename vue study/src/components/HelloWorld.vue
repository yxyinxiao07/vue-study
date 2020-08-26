<template>
  <div class="hello">
    <span>parentmsg:{{parentmsg}}</span>
    <button @click="changeChild">给父组件传值</button>
    <h1 style="background:red">{{ msg }}</h1>
    <h1 :style="newstyle">{{ msg }}</h1>
    <h1 style="height:100px" :style="newstyle">{{ msg }}</h1>
    <h1 style="height:100px" :class="style1">{{ msg }}</h1>
    <h1 class="bgRed">{{ msg }}</h1>
    <h1 :class="style1">{{ msg }}</h1>
    <h1 :class="style2">{{ msg }}</h1>
    <h1 class="abc" :class="style1">{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      childmsg: '22222',
      msg: '123123',
      style1: 'bgRed',
      style2: ['bgRed', 'abc'],
      newstyle: {
        background: 'skyblue',
        borderBottom: '1px solid red'
      }
    }
  },
  props: ['parentmsg'],
  methods: {
    changeChild () {
      this.childmsg = Math.ceil(Math.random() * 10)
      this.$emit('childmsg', this.msg)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.bgRed {
  background: brown;
}
.abc {
  height: 200px;
}
</style>
