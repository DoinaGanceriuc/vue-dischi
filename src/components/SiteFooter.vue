<template>
  <footer id="site_footer">
    <div class="container">
      <div class="copyright">
        <small class="text-white" >Boolean</small>
      </div>
    </div>
    <!-- /.container -->
  </footer>
  <!-- /#site_footer -->
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
footer {
  height: 100px;
  background-color: $bg_dark_top;
.copyright {
  line-height: 100px;
  vertical-align: middle;
  text-align: center;
}
}
</style>
