<template>
<div>
  <h1>我是2组件</h1>
  <p>我是冲组件1中接收的参数：{{msgs}}</p>

</div>
</template>
<script>
import bus from './event.js'
export default {
  name: 'first',
  data() {
    return {
      msgs: '我是默认值握'
    }
  },
  mounted() {
    console.log('tag', self)
    var self = this
    bus.$on('data', function(val) {
      console.log('tag', val)
      self.msgs = val
    })
  }
}
</script>
