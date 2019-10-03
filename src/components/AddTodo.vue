<template>
    <div>
        <form>
            <input type="text" class="">
            <input type="submit" class="btn">
        </form>
    </div>
</template>
<script>
export default {
    
}
</script>
<style scoped>
    form{
        display: flex;
    }
    input[type="text"]{
        flex: 4;
        font-weight: bold;
        font-size: 36px;
        padding: 20px; 
        border-bottom: 1px dashed #011521; 
    }
    input[type="submit"]{
        color: #011521;
        background: #fff;
        flex: 1;
        border-left: 1px dashed #011521;
        border-bottom: 1px dashed #011521;
    }
    input[type="submit"]:hover{
        transition: .7s;
        color: #f0f0f0;
        background: #011521;
        cursor: pointer;
    }
</style>