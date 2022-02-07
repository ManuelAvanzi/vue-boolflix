<template>
    
 <div class="stars-container">


             <i v-for="(star, index) in stars" :key="index">&#9733;</i>

            
    </div>
</template>


<script>


export default {
    props:{
        score: Number,
    },


    computed: {

        stars() {
            return Math.ceil(this.score / 2)
        }
    }
}
</script>



<style lang="scss" scoped>
.stars-container{
    display: flex;
    
    padding:5px;
    i{
       
        color:rgba(255, 255, 0, 0.886);
    }
}

</style>