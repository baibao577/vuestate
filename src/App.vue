<template>
  <div id="app">
    <div class="container">
      <img alt="Vue logo" src="./assets/logo.png">
      <AddTodo />
      <Todos />
    </div>
  </div>
</template>

<script>
import Todos from './components/Todos.vue'
import AddTodo from './components/AddTodo.vue'

export default {
  name: 'app',
  components: {
    Todos,
    AddTodo
  }
}
</script>

<style>
.container {
  max-width: 500px;
  margin: auto;
}
</style>
