<template>
    <div class="header-box">

      <div class="title-container">
        <h1>Boolflix</h1>
      </div>

      <search-bar/>
    </div>
</template>


<script>
import SearchBar from './SearchBar.vue'

export default {
    components:{
        SearchBar
    }
}
</script>



<style lang="scss" scoped>
 
 .header-box{
     background-color: rgba(0, 0, 0, 0.932);
     display: flex;
     justify-content: space-between;
     .title-container{
      
       padding:5px 10px;
             
     h1{
         color:rgb(216, 0, 0);
       }
     }
 }

</style>