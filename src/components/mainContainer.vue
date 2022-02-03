<template>
    <div class="main-box">

  <!--per ogni elemento in elenco passo la prop-->
         <film-card
                v-for="movie in elenco"
                :key="movie.id"
                :card="movie" />

    </div>

</template>


<script>
import filmCard from './filmCard.vue'
export default {
  components: {
       filmCard 
       },

       props: {

         elenco: Array,
       
       },
    
}
</script>


<style lang="scss" scoped>
.main-box{
    margin:0 auto;
    width: 90%;
    
    background-color: black;
    padding:20px;

    border:1px solid white;
    display: flex;
    flex-wrap: wrap;
    
    film-card{
        
    }
    
}

</style>