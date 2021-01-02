<template>
  <h1>TodoList com Vue.js 3!</h1>
  <TodoList/>
</template>

<script>
import TodoList from './components/TodoList.vue'

export default {
  name: 'App',
  components: {
    TodoList
  }
}
</script>

<style>
</style>
