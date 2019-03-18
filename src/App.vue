<template>
  <div id="app">
    <jishuqi :initnum="20" :dfmax="30" :dfmin="0" :bushu="3"></jishuqi>
  </div>
</template>

<script>
import jishuqi from "./components/jishuqi"
export default {
  name: 'app',
  components:{
    jishuqi
  }
}
</script>

<style lang="scss">
  
</style>