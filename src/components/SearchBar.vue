<template>

    <div class="container">
        <input v-model="filmString" type="text">
        <button id="button" @click="searchFilm">Search</button>    
    </div>
</template>


<script>
export default {

    data(){
        return {

         // Questa potrebbe essere la stringa che passerò alla funzione che farà la chiamata API
         filmString:"",

         stringA:"https://api.themoviedb.org/3/search/movie?query=",
         stringB:"&api_key=f92de852056df36bad71c98feade9c89",

         myQuery:"",
        }
    },
    methods:{


          // Semplice funzione per capire se è tutto ok 
        searchFilm:function(){

            //controllo nel terminale ogni passaggio che non si sa mai 
            console.log(`${this.filmString}`);
            console.log(`${this.stringA}`);
            console.log(`${this.stringB}`);
            
            



            this.myQuery=this.stringA + this.filmString+ this.stringB;
            console.log(`questa è la query che manderò ${this.myQuery}`);
            this.filmString="";


        }
    }
}
</script>


<style lang="scss" scoped>
.container{
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
</style>