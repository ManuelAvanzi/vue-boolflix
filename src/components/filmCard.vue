<template>
    
        <div class="info-card">
            <div class="text">{{card.title}}</div>
            <div class="text">{{card.original_title}}</div>
            <div class="text">{{card.original_language}}</div>
            <div class="text">{{card.vote_average}}</div>
            
        </div>
       
    
</template>

<script>
export default {

    props: {
        card: Object
    },
}
</script>

<style lang="scss" scoped>

.info-card{
    border:1px solid white;
    width:150px;
    height: 230px;
    background-color: rgb(16, 85, 85);
    text-align: center;
    margin:5px;
    border-radius:5px;

    h1{
        color:white;
        
    }
    .text{
        color:white;
    }
}


</style>