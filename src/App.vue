<template>
  <div id="app">
    <header-container/>
    <main-container :albums="albums"/>
  </div>
</template>

<script>
import HeaderContainer from './components/HeaderContainer.vue'
import MainContainer from './components/MainContainer.vue'
import axios from 'axios'

export default {
  name: 'App',
  components: {
    HeaderContainer,
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
