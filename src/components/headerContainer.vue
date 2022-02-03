<template>
    <div class="header-box">

      <div class="logo-container">
        <h1>Boolflix</h1>
      </div>

      <!--sostituisco un componenete con un più semplice div-->

      <div class="input-container ">
        <input v-model="filmString" type="text">
        <button id="button" @click="searchFilm">Search</button>    
      </div>

    </div>
</template>


<script>


export default {
    components:{
        
    },
    data(){
        return {

         // stringa che ricevo dal utente
         filmString:"",

         stringA:"https://api.themoviedb.org/3/search/movie?query=",
         stringB:"&api_key=f92de852056df36bad71c98feade9c89",
          
         // stringA + filmstring + stringB
         myQuery:"",
        }
    },
    methods:{


        
        searchFilm:function(){

            this.myQuery=this.stringA + this.filmString+ this.stringB,
            console.log(`questa è la query che manderò : ${this.myQuery}`);
            this.filmString="";

            
            
        },

        

    },
}
</script>



<style lang="scss" scoped>
 
 .header-box{
     background-color: rgba(0, 0, 0, 0.932);
     display: flex;
     justify-content: space-between;

     .input-container{
    input{
        border:2px solid orange;
        border-radius: 5px;
        padding:4px;
        margin-top:10px;
        

    }
    button{
        padding:5px 10px;
        border:2px solid orange;
        border-radius:5px;
        margin:0 15px;
        margin-right:25px;
        cursor: pointer;
        background-color: rgba(252, 252, 252, 0.548);
        color:white;
    }
    button:hover{
        border:2px solid lime;
        background-color: rgba(253, 230, 230, 0.856);
    }

}
     .logo-container{
      
       padding:5px 10px;
             
     h1{
         color:rgb(216, 0, 0);
       }
     }
 }

</style>