<template>
  <div id="app">
    <Header />
    <AddTodo />
    <TodoRows />
  </div>
</template>

<script>
import AddTodo from './components/AddTodo';
import TodoRows from './components/Todo.rows';
import Header from './components/layout/Header';


export default {
  name: "app",
  components: {
    Header,
    AddTodo,
    TodoRows
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
