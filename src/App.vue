<template>
  <div id="app">
    <header-box/>
    <select-box @search="filterGenre"/>
    <app-loader v-if="!loaded"/>
    <main-container v-else :albums="albumsFiltered"/>
  </div>
</template>

<script>
import HeaderBox from './components/HeaderBox.vue'
import SelectBox from './components/SelectBox.vue'
import AppLoader from './components/AppLoader.vue'
import MainContainer from './components/MainContainer.vue'
import axios from 'axios'

export default {
  name: 'App',
  components: {
    AppLoader,
    HeaderBox,
    SelectBox,
    MainContainer
  },
  data() {
    return {
      albums: [],
      albumsFiltered: [],
      loaded: false
    }
  },
  mounted() {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((result) => {
      this.albums = result.data.response
      this.albumsFiltered = result.data.response
      this.loaded = true
    })
  },
  methods: {
    filterGenre(genre) {
      this.albumsFiltered = this.albums.filter((album) =>{
        return album.genre.toLowerCase() === genre || genre === 'all';
      })
    }
  }
}
</script>

<style lang="scss">
@import './style/common.scss';
@import './style/variables.scss';
</style>
