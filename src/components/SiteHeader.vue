<template>
  <header id="site_header">
    <div class="container d-flex justify-content-between align-items-center">
      <div class="logo text-start align-middle">
        <img width="50" src="../assets/spotify-logo.png" alt="" />
      </div>
      <div>
        <select class="form-select" aria-label="">
          <option selected>Select genre</option>
          <option value="Rock">Rock</option>
          <option value="Pop">Pop</option>
          <option value="Jazz">Jazz</option>
          <option value="Metal">Metal</option>
        </select>
      </div>
    </div>
    <!-- /.container -->
  </header>
  <!-- /#site_header -->
</template>

<script>
export default {}
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
