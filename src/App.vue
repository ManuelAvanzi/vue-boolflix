<template>
  <div id="app">
    <header-container />
    <main-container/>
  </div>
</template>

<script>

//API Key: f92de852056df36bad71c98feade9c89
//https://api.themoviedb.org/3/search/movie?api_key=f92de852056df36bad71c98feade9c89 
//import axios from 'axios'
import HeaderContainer from './components/headerContainer.vue'
import MainContainer from './components/mainContainer.vue'


export default {
  name: 'App',
  components: {
    HeaderContainer,
    MainContainer,
  },
  data(){
    return {
      films:[]
    }
  },
  methods:{

    // passo ad axios la stringa che viene da film card che viene da header
      //cercaFilm(myQuery){

        // return axios.get('myQuery').then((response)=>{
         //this.films=response.data.results
         //console.log(response.data.results);
      //})
  }
  }

</script>

<style lang="scss">
@import './style/main.scss'
</style>
