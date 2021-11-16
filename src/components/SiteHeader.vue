<template>
  <header id="site_header">
    <div class="container d-flex justify-content-between align-items-center">
      <div class="logo text-start align-middle">
        <img width="50" src="../assets/spotify-logo.png" alt="" />
      </div>
    </div>
    <!-- /.container -->
  </header>
  <!-- /#site_header -->
</template>

<script>
/* import SelectAlbum from '../components/SelectAlbum.vue' */
export default {
  /*  components: {
    SelectAlbum
  } */
}
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";
header {
  height: 100px;
  background-color: $bg_dark_top;
  .logo {
    line-height: 100px;
  }
}
</style>
