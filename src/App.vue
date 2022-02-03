<template>
  <div id="app">
    <!--@nome evento custom ="nome della funzione in App.vue che userà il valore passato"-->
    <header-container @search="cercaFilm"/>
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

      
      //cercaFilm ora parte ogni volta che viene premuto il pulsante 
      //userQuery è la variabile che ho definito in headerContainer.vue
      cercaFilm(userQuery){
        console.log(userQuery);
      }       
   },
                                           
  }

</script>

<style lang="scss">
@import './style/main.scss'
</style>
