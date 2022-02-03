<template>
  <div id="app">
    <header-container/>
    <main-container/>
  </div>
</template>

<script>
import HeaderContainer from './components/headerContainer.vue'
import MainContainer from './components/mainContainer.vue'


export default {
  name: 'App',
  components: {
    HeaderContainer,
    MainContainer,
  }
}
</script>

<style lang="scss">
@import './style/main.scss'
</style>
