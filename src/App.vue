<template>
  <div id="app">
    <main-container :albums="albums"/>
  </div>
</template>

<script>
import MainContainer from './components/MainContainer.vue'
import axios from 'axios'

export default {
  name: 'App',
  components: {
    MainContainer
  },
  data() {
    return {
      albums: {}
    }
  },
  mounted() {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((result) => {
      this.albums = result.data
    })
  }
}
</script>

<style lang="scss">
@import './style/common.scss';
</style>
