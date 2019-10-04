<template>
  <div id="app">
    <Header />
    <AddTodo v-on:add-todo="addTodo"/>
    <Todos v-bind:todos="todos" v-on:del-todo="deleteTodo"/>
  </div>
</template>

<script>
import AddTodo from './components/AddTodo';
import Todos from './components/Todos';
import Header from './components/layout/Header';


export default {
  name: "app",
  components: {
    Header,
    AddTodo,
    Todos
  },
    data(){
    return {
      todos:[
        {
          id: 1,
          title: "Todo One",
          completed: false
        },
        {
          id: 2,
          title: "Todo Two",
          completed: true
        },
        {
          id: 3,
          title: "Todo Three",
          completed: false
        }
      ]
    }
  },
  methods: {
    deleteTodo(id){
      this.todos = this.todos.filter(todo => todo.id !== id)
    },
    addTodo(Adding){
      this.todos = [...this.toods, Adding];
    }
  }
};
</script>
<style>
@import url('https://fonts.googleapis.com/css?family=Playfair+Display&display=swap');
*{
  font-family: 'Playfair Display', serif;
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

</style>
