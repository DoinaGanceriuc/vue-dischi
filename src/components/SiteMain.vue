<template>
  <main id="site_main">
    <div class="container">
        <div class="row row-cols-md-6 gx-5 py-5 justify-content-center">
  <div class="col py-3" v-for="poster in posters" :key="poster.id">
    <div class="card h-100">
      <img :src="poster.poster" class="card-img-top" width="50" :alt="poster.author">
      <div class="card-body">
        <h5 class="card-title">Card title</h5>
        <p class="card-text">This is a longer card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
      </div>
    </div>
  </div>
</div>
    </div>

  </main>
  <!-- /#site_main -->
</template>

<script>
import axios from 'axios'
export default {

  data () {
    return {
      posters: [],
      API_URL: 'https://flynn.boolean.careers/exercises/api/array/music'
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
  background-color: #1E2D3B;
}

</style>
