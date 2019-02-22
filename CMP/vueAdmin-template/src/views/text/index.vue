<template>
<div style="padding:40px">
   <first-child></first-child>
   <second-child></second-child>
</div>
</template>
<script>
import firstChild from './firstChild'
import secondChild from './secondChild'
export default {
  name: 'text',
  components: {
    firstChild, secondChild
  }
}
</script>

