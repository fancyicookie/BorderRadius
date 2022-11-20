<!--
 * @Date: 2022-11-17 15:12:57
 * @Author: Fancyicookie
-->
<template>
  <div id="app">
    <h2>Border-Radius-Preview</h2>
    <hr style="width: 350px"/>
    <!-- <BorderRadius /> -->
    <BorderRadius_computed />
  </div>
</template>

<script>
// import BorderRadius from './components/BorderRadius.vue'
import BorderRadius_computed from './components/BorderRadius_computed.vue'

export default {
  name: 'App',
  components: {
    // BorderRadius,
    BorderRadius_computed
  }
}
</script>

<style lang="less">
#app {
  margin: 0 auto;
  text-align: center;
  width: 100%;
  height: 100%;
  background-color: rgb(33, 31, 70);
  position:fixed;
  color: azure;
}
</style>
