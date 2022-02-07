<template>
    

     <div class="info-card">
       <img :src=" `https://image.tmdb.org/t/p/original${movie.poster_path}` ">
        <div class="info">
            <h3>{{movie.title}}</h3>
            <ul>
                <li><span class="movie-info">Titolo Originale:</span> {{movie.original_title}}</li>
                
                <li>punteggio :<score-box :score="movie.vote_average"/></li>

                <li><span class="movie-info">Lingua:</span> </li>
                <li><img :src="`/flags/${movie.original_language}.png`" :alt="movie.original_language"></li>    
            </ul>
           
            
        </div>
    </div>
</template>
    
        

<script>
import scoreBox from './scoreBox.vue'




export default {
 
    components: {
        
        scoreBox,
    },
   
    props: {
        movie: Object
    },
}
</script>

<style lang="scss" scoped>



     .info-card {
         background-color: white;
         color: white;
         margin: 10px;
         width: calc(20% - 30px);
         min-height: 100%;
         max-height: 480px;
         position: relative;
         cursor: pointer;
         img {
             width: 100%;
             height: 100%;

             object-fit: cover;
         }
         &:hover .info {
             display: block;
         }
         .info {
             padding: 30px;
             background: black;
             position: absolute;
             top: 0;
             left: 0;
             bottom: 0;
             right: 0;
             display: none;
             
             h3 {
                 margin-bottom: 20px;
             }
             ul {
                 margin-bottom: 20px;
                 li {
                     list-style: none;
                     font-weight: normal;
                     margin-top: 10px;
                     font-size: 11px;
                     width: 80%;
                 }
                 .flag-img{
                     width:50px;
                 }
             }
             &::after {
                 content: '';
                 flex: auto;
             }
             .movie-info {
                 color: white;
                 
             }
         }
     }
</style>