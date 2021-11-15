<template>
  <div id="app">
    <Siteheader/>
    <SiteMain/>
  </div>
</template>

<script>
import Siteheader from './components/SiteHeader.vue'
import SiteMain from './components/SiteMain.vue'

export default {
  name: 'App',
  components: {
    Siteheader,
    SiteMain
  }
}
</script>

<style lang="scss">
@import '../node_modules/bootstrap/scss/bootstrap.scss';
@import './assets/scss/common.scss';
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
