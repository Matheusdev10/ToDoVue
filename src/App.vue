<template>
  <div>
    <h2>Todos em aberto</h2>
    <div v-for="todo in incompletedTodos" :key="todo.id">
      {{ todo.title }}
    </div>

    <h2>Todos completas</h2>
    <div v-for="todo in completedTodos" :key="todo.id">
      {{ todo.title }}
    </div>

    <br /><br /><br />

    <h2>Todos</h2>
    <div v-for="todo in todos" :key="todo.id">
      <input v-model="todo.completed" type="checkbox" />
      {{ todo.title }}
    </div>
  </div>
  <br />
</template>

<script setup>
import { computed } from 'vue';
import { todos } from './todo.vue';

const completedTodos = computed(() => {
  return todos.value.filter((todo) => todo.completed);
});

const incompletedTodos = computed(() => {
  return todos.value.filter((todo) => !todo.completed);
});
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 60px;
}
</style>
