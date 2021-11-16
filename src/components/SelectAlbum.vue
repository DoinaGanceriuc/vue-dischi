<template>
      <div>
        <select v-model="selected" class="form-select" aria-label="" @change="$emit('selectAlbums', selected)">
          <option selected>Select genre</option>
          <option value="Rock">Rock</option>
          <option value="Pop">Pop</option>
          <option value="Jazz">Jazz</option>
          <option value="Metal">Metal</option>
        </select>
      </div>
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
