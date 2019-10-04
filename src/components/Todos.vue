<template>
    <div>
        <div v-bind:key="todo.id" v-for="todo in todos">
            <TodoRows v-bind:todo="todo" v-on:del-todo="$emit('del-todo', todo.id)" />
        </div>
    </div>
</template>
<script>
import TodoRows from './Todo.rows.vue';

export default {
    name: "Todos",
    components:{
        TodoRows
    },
    props: ["todos"]
}
</script>
<style scoped>

</style>