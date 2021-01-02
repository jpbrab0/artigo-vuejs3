<template>
  <div class="app">
    <ol>
      <li v-for="todo in todos" v-bind:key="todo.id">
        <p>{{ todo.text }}</p>
      </li>
    </ol>
    <div class="inputs">
      <input placeholder="Todo" v-model="text" />
      <div class="buttons">
        <button v-on:click="addTodo(text)">Adicionar Tarefa</button>
        <button v-on:click="removeTodos()">Remover Todas as tarefas</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      todos: [{ id: 1, text: "Aprender VueJs" }],
    };
  },
  methods: {
    addTodo(text) {
      if (text !== " ") {
        this.todos.push({
          id: this.todos.length + 1,
          text,
        });
      }
    },
    removeTodos() {
      this.todos = [];
    },
  },
};
</script>

<style>
</style>