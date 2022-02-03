<template>
    <div class="header-box">

      <div class="logo-container">
        <h1>Boolflix</h1>
      </div>

      <!--sostituisco un componenete con un più semplice div-->

      <div class="input-container ">
        <input v-model="filmString" type="text">


      <!--quando premo il button passa ad App.vue la stringa inserita -->
      <!--al click creo un evento custom chiamato search a cui passo filmstring che continene la stringa inserita -->
        <button id="button" @click="$emit('search' , filmString)">Search</button>    
      </div>

    </div>
</template>


<script>


export default {
    data(){
        return {

         // stringa che ricevo dal utente
         filmString: "",
         
        }
    },
    methods:{

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