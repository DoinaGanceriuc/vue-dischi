<template>
  <main id="site_main">
    <div class="container">
      <div class="row row-cols-md-6 gx-5 py-5 justify-content-center">
        <div class="col py-3" v-for="poster in posters" :key="poster.id">
          <div class="card h-100 align-items-center">
            <img
              :src="poster.poster"
              class="card-img-top"
              :alt="poster.author"
            />
            <div class="card-body text-center">
              <h5 class="card-title text-white">
                {{ poster.title.toUpperCase() }}
              </h5>
              <p class="card-text text-muted m-0">{{ poster.author }}</p>
              <p class="card-text text-muted">{{ poster.year }}</p>
            </div>
          </div>
            <!-- /.card -->
        </div>
          <!-- /.col -->
      </div>
        <!-- /.row -->
    </div>
    <!-- /.container -->
  </main>
  <!-- /#site_main -->
</template>

<script>
import axios from 'axios'
export default {

  data () {
    return {
      posters: [],
      API_URL: 'https://flynn.boolean.careers/exercises/api/array/music',
      loading: true
    }
  },
  mounted () {
    axios
      .get(this.API_URL)
      .then(response => {
        console.log(response)
        this.posters = response.data.response
        console.log(this.posters)
        this.loading = false
      }).catch(error => {
        console.log(error)
      })
  }

}
</script>

<style lang="scss">
main {
  background-color: #1e2d3b;
  height: calc(100vh - 100px);
  .card {
    background-color: #2e3a46;

    .card-img-top {
      width: 130px;
      height: 130px;
      padding-top: 1rem;
    }
  }
}
</style>
