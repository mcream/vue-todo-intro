<template>
    <div class="todo-rows" v-bind:class="{'completed':todo.completed}">
        <p>
            <input type="checkbox" v-on:change="markComplete">
            {{ todo.title }}
            <button @click="$emit('del-todo', todo.id)" class="del">DELETE</button>
        </p>
    </div>
</template>
<script>
export default {
    name: "TodoRows",
    props: ["todo"],
    methods: {
        markComplete(){
            this.todo.completed = !this.todo.completed;
        }
    }
}
</script>
<style scoped>
.todo-rows{
    background: #76a2bd;
    padding: 20px;
    border-bottom: 1px #ccc dotted;
}
.del{
    background: #be3535;
    color: #f5f5f5;
    border: none;
    padding: 5px 9px;
    border-radius: 10%;
    cursor: pointer;
    float: right;
}
.del:hover{
    transition: .4s;
    background: #d84646;
}
.completed{
    color: #adadad;
}
</style>