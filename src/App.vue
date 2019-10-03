<template>
  <div id="app">
    <AddTodo />
  </div>
</template>

<script>
import AddTodo from './components/AddTodo';

export default {
  name: "app",
  components: {
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
