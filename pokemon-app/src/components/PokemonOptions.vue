<template>
    <div class="options-container" >
        <ul>
            <li></li>
            <li></li>
            <li></li>
            <li></li>
        </ul>
    </div>
</template>

<script>
export default {
    
}
</script>


<style scoped>
   ul{
    list-style-type: 0;
   }
   li {
        background-color: aliceblue;
        border-radius: 5px;
        border: 1px solid rgb(0,0,0,0.2);
        cursor: pointer;
        margin-bottom: 10px;
        width: 250px;
    }

    li:hover{
        background-color: rgb(0,0,0,0.05);
    }

    .options-container {
        display: flex;
        justify-content: center;
    }
</style>