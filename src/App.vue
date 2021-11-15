<template>
  <div id="app">
    <Siteheader/>
  </div>
</template>

<script>
import Siteheader from './components/SiteHeader.vue'

export default {
  name: 'App',
  components: {
    Siteheader
  }
}
</script>

<style lang="scss">
@import '../node_modules/bootstrap/scss/bootstrap.scss';
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
