<template>
    <div class="container">
        <input type="text" placeholder="cerca un film">
        <button>SEARCH</button>
    </div>
</template>


<script>
export default {
    
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