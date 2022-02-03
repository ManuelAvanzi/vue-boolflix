<template>
    <div class="main-box">

         <film-card/>

    </div>

</template>


<script>
import filmCard from './filmCard.vue'

export default {
  components: { filmCard },
    
}
</script>


<style lang="scss" scoped>
.main-box{
    width: 100%;
    height: 1000px;
    background-color: rgba(128, 128, 128, 0.966);
    padding:20px;

    
}

</style>