<template>
  <div id="app">
    <!--@nome evento custom ="nome della funzione in App.vue che userà il valore passato"-->
    <header-container @search="cercaFilm"/>
    
    <main-container :films="films" :series="series" lingua="linguaggi"/>
  </div>
</template>

<script>

//API Key: f92de852056df36bad71c98feade9c89
import axios from 'axios'
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
      api_key:'f92de852056df36bad71c98feade9c89',
      films: [],
      series: [],
      linguaggi:['italiano','brazilian','france','german','india','norway','portugal','uk']

    }
  },
  methods:{

      
     
      //userQuery è la variabile che ho definito in headerContainer.vue
      cercaFilm(userQuery){
        
        

        //ricerco il film partendo dalla userQuery
        axios.get(`https://api.themoviedb.org/3/search/movie?query=${userQuery}&api_key=f92de852056df36bad71c98feade9c89`)
        .then((response) => {
          this.films = response.data.results;
        });

        //ricerco la serie partendo dalla userQuery
        axios.get(`https://api.themoviedb.org/3/search/tv?query=${userQuery}&api_key=f92de852056df36bad71c98feade9c89`)
        .then((response) => {
          this.series = response.data.results;
          
        });
        
       

      
      }       
   },
 
     
   
                                           
  }

</script>

<style lang="scss">
@import './style/main.scss'
</style>
