<template>

<main>
    
    <div class="section-title"><h1>FILM</h1></div>

    <!--FILMS-->
    <div class="container-film">
        <film-card v-for="movie in films" 
                :key="movie.id"
                :movie="movie" />
    </div>

    <div class="section-title"><h1>SERIE</h1></div>
    

    <!--SERIE-->
    <div class="container-serie">
            <tv-card v-for="show in series" 
                :key="show.id"
                :show="show"/>
    </div>
</main>
    

</template>


<script>

import TvCard from '@/components/TvCard.vue'
import filmCard from '@/components/filmCard.vue'


export default {
  components: {
        filmCard,
        TvCard
    },
    props: {
        films: Array,
        series: Array,
    }
}
</script>


<style lang="scss" scoped>
  main {
        width: 90%;
        
        margin: 0 auto;

        .section-title{
            
            margin:10px;
            h1{
                color:white;
                padding:10px;
            }
        }
      
        .container-film{
            
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
        }
        .container-serie{
            

            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
        }
        


    }

</style>