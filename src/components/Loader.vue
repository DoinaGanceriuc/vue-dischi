<template>
  <div class="loader" v-if="!loading">
    <div class="row row-cols-md-6 gx-5 py-5 justify-content-center">
      <div class="col py-3" v-for="poster in posters" :key="poster.id">
        <div class="card h-100 align-items-center">
          <img :src="poster.poster" class="card-img-top" :alt="poster.author" />
          <div class="card-body text-center">
            <h5 class="card-title text-white">
              {{ poster.title.toUpperCase() }}
            </h5>
            <p class="card-text text-muted m-0">{{ poster.author }}</p>
            <p class="card-text text-muted">{{ poster.year }}</p>
          </div>
        </div>
        <!-- ./card -->
      </div>
      <!-- ./col -->
    </div>
    <!-- ./row -->
  </div>
  <!-- ./loader -->
  <div v-else>
    <h3 class="text-white">Loading...</h3>
  </div>
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
  methods: {
    callApi () {
      axios
        .get(this.API_URL)
        .then((response) => {
          console.log(response)
          this.posters = response.data.response
          console.log(this.posters)
          this.loading = false
        })
        .catch((error) => {
          console.log(error)
        })
    }
  },
  mounted () {
    setTimeout(this.callApi, 2000)
  }
}
</script>

<style lang="scss"></style>
