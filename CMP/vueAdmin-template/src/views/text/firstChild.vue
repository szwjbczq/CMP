<template>
  <div>
    <h1>我是1组件</h1>
    <button @click="send">向组件传值</button>
    {{msg}}}
  </div>
</template>
<script>
import bus from './event.js'
export default {
  name: 'first',
  data() {
    return {
      msg: '我是组见11111hahah'
    }
  },
  methods: {
    send() {
      bus.$emit('data', this.msg)
    }
  }
}
</script>

