<template>
  <header id="site_header">
    <div class="logo text-start align-middle container">
       <img width="50" src="../assets/spotify-logo.png" alt="">
    </div>
    <!-- /.container -->
  </header>
  <!-- /#site_header -->
</template>

<script>
export default {

}
</script>

<style lang="scss">
@import '../assets/scss/variables.scss';
header {
  height: 100px;
  background-color: $bg_dark_top;
  .logo {
    line-height: 100px;
  }
}

</style>
