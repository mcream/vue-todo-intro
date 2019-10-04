<template>
    <div>
        <div v-for="todo in todos">
            <TodoRows />
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