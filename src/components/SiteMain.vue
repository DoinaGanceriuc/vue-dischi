<template>
  <main id="site_main">
    <div class="container">
      <Loader/>
    </div>
    <!-- /.container -->
  </main>
  <!-- /#site_main -->
</template>

<script>
// import axios from 'axios'
import Loader from '../components/Loader.vue'
export default {
  components: {
    Loader
  }
}
</script>

<style lang="scss">
@import '../assets/scss/variables.scss';
main {
  background-color: $bg_dark_contain;
  height: calc(100vh - 200px);
  overflow: auto;
  .card {
    background-color: $bg_dark_top;

    .card-img-top {
      width: 90%;
      padding-top: 1rem;
    }
  }
}
</style>
