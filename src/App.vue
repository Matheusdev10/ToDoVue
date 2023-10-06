<script setup>
import { ref } from 'vue';
import Input from './components/Input.vue';
import Button from './components/Button.vue';

const tarefa = ref('');

const todo = async () => {
  const dados = {
    inputTarefa: tarefa.value,
  };
  console.log(dados);
};
</script>

<template>
  <container>
    <h1 class="bg-primary d-flex justify-content-center p-4">TO DO LIST</h1>

    <div
      class="d-flex justify-content-center bg-secondary align-items-center gap-3"
      style="height: 100vh"
    >
      <form ref="getDados" @submit.prevent="todo($event)">
        <Input
          @submit.prevent="login($event)"
          type="text"
          v-model="tarefa"
          placeholder="Digite sua tarefa"
        />
        <Button type="submit" title="adicionar" />
      </form>
    </div>
  </container>
</template>
