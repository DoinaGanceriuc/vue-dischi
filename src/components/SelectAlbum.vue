<template>
      <form>
        <select v-model="selected" class="form-select" aria-label="" @change.prevent="$emit('selectAlbums', selected)">
          <option value="">Choose genre...</option>
          <option value="All">All albums</option>
          <option value="Rock">Rock</option>
          <option value="Pop">Pop</option>
          <option value="Jazz">Jazz</option>
          <option value="Metal">Metal</option>
        </select>
      </form>
</template>

<script>
export default {
  data () {
    return {
      selected: ''
    }
  },
  methods: {
    selectAlbums (optionSelected) {
      console.log(optionSelected)
      console.log(this.selected)
    }
  }
}
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";
form {
  padding-top: 1rem;
}
</style>
