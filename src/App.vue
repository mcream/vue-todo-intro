<template>
  <div id="app">
    <Header />
    <AddTodo />
  </div>
</template>

<script>
import AddTodo from './components/AddTodo';
import Header from './components/layout/Header';


export default {
  name: "app",
  components: {
    Header,
    AddTodo
  }
};
</script>
<style>
*{
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

</style>
