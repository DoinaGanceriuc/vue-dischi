<template>
  <div class="loader" v-if="!loading">
    <SelectAlbum @selectAlbums="select" />
    <div class="row row-cols-2 row-cols-sm-3 row-cols-xl-6 py-5 justify-content-center">
      <div class="col py-3" v-for="poster in getFilteredAlbums" :key="poster.id">
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
import SelectAlbum from '../components/SelectAlbum.vue'
export default {
  components: {
    SelectAlbum
  },
  data () {
    return {
      posters: [],
      API_URL: 'https://flynn.boolean.careers/exercises/api/array/music',
      loading: true,
      optionSelected: ''
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
    },
    select (elementoSelezionato) {
      console.log(elementoSelezionato)
      this.optionSelected = elementoSelezionato
    /* console.log(this.optionSelected) */
    }
  },
  mounted () {
    setTimeout(this.callApi, 2000)
  },
  computed: {
    getFilteredAlbums () {
      if (this.optionSelected === 'All') {
        return this.posters
      }
      const filteredAlbums = this.posters.filter((poster) => {
        return poster.genre.includes(this.optionSelected)
      }
      )
      return filteredAlbums
    }
  }
}
</script>

<style lang="scss">
.loader {
  display: flex;
    flex-direction: column;
    align-items: center;
}
</style>
