<template>
    <div>
        <form>
            <input type="text" v-model="title" class="" placeholder="Add">
            <input type="submit" class="btn">
        </form>
    </div>
</template>
<script>
import uuid from 'uuid';

export default {
    name: "AddTodo",
    data(){
        return{
            title: ''
        }
    },
    methods: {
        addTodo(e){
            e.preventDefault();
            const adding = {
                id: uuid.v4(),
                title: this.title,
                completed: false
            }
            this.$emit('add-todo', adding);
        }
    }
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