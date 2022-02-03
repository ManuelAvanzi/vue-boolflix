<template>
  <div id="app">
    <header-container/>
  </div>
</template>

<script>
import HeaderContainer from './components/headerContainer.vue'


export default {
  name: 'App',
  components: {
    HeaderContainer,
  }
}
</script>

<style lang="scss">
@import './style/main.scss'
</style>
