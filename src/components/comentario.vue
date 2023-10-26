<!-- DIRETIVASV V-SHOW -->
<!-- (v-show) o elemento fica na dom 
ex: declaro a diretiva v-show no componente e crio uma variavel chamada showHeader -->
<!-- declaro ela false, ela some da tela, mas não some da dom -->
<!-- se usar o v-if, ela some da dom -->

<!-- <template>
  <TheHeader
  v-show = "showHeader"
  
  />
</template>

<script>
const showHeader = ref(false)

function showTheHeader(){
  return showHeader
}
showTheHeader()
</script> -->

<!-- DIRETIVA V-IF condicionais -->

<!-- <template>
  <div v-if="msg === 'ola'">
    <Input />
  </div>
</template>

<script>
const msg = ref('ola');
</script> -->

<!--DIRETIVA  v-for -->
<!-- 
<div v-for="(todo, index) in todos" v-bind:key="todo.id">
  {{ index }} -
  {{ todo.title }}
  {{ todo.userId }}
  {{ todo.completed }}
</div> -->

<!-- export const todos = [
  {
    userId: 1,
    id: 1,
    title: 'Estudar reactjs',
    completed: false,
    urlImg: "https://via.placeholder.com/150/24f355"
  },
  {
    userId: 1,
    id: 2,
    title: 'estudar vuejs',
    completed: false,
    urlImg: "https://via.placeholder.com/150/d32776"

  },
  {
    userId: 1,
    id: 3,
    title: 'estudar boostrap',
    completed: false,
    urlImg: "https://via.placeholder.com/150/f66b97"
  },
  {
    userId: 1,
    id: 4,
    title: 'estudar js',
    completed: true,
    urlImg: "https://via.placeholder.com/150/56a8c2"
  },
  {
    userId: 1,
    id: 5,
    title: 'estudar php',
    completed: true,
    urlImg: "https://via.placeholder.com/150/b0f7cc"
  },
]; -->

<!-- DIRETIVA V-BIND -->
<!-- v-bind é usado para identificar 
  que o atributo passado sera dinamico (bind no ingles é ligar) -->

<!-- <div v-for="(todo, index) in todos" v-bind:key="todo.id">
    <img v-bind:src="todo.urlImg" v-bind:alt="todo.imgAlt" />
    {{ index }} -
    {{ todo.title }}
    {{ todo.userId }}
    {{ todo.completed }}
  </div> -->

<!-- exemplo de dados mocados -->

<!-- export const todos = [
  {
    userId: 1,
    id: 1,
    title: 'Estudar reactjs',
    completed: false,
    urlImg: 'https://via.placeholder.com/150/24f355',
    imgAlt: 'img1',
  },
  {
    userId: 1,
    id: 2,
    title: 'estudar vuejs',
    completed: false,
    urlImg: 'https://via.placeholder.com/150/d32776',
    imgAlt: 'img2',
  },
  {
    userId: 1,
    id: 3,
    title: 'estudar boostrap',
    completed: false,
    urlImg: 'https://via.placeholder.com/150/f66b97',
    imgAlt: 'img3',
  },
  {
    userId: 1,
    id: 4,
    title: 'estudar js',
    completed: true,
    urlImg: 'https://via.placeholder.com/150/56a8c2',
    imgAlt: 'img4',
  },
  {
    userId: 1,
    id: 5,
    title: 'estudar php',
    completed: true,
    urlImg: 'https://via.placeholder.com/150/b0f7cc',
    imgAlt: 'img5',
  },
]; -->

<!-- DIRETIVA V-MODEL -->
<!-- Utilizada principalmente para formularios (input, radio, select) -->
<!-- consegue alterar o valor em duas direções -->
<!-- tanto pelo sistema, quando pelo usuario que usa o sistema -->

<!-- exemplo -->
<!-- 

<script setup>
import { ref } from 'vue'

const newsletter = ref("")
</script>

<template>

<div>

<input
v-model="newsletter"
type="radio"
value="sim"
>
sim

<input
v-model="newsletter"
type="radio"
value="nao"
>
nao
<br>

{{newsletter}}
</div>
</template>

 -->

<!-- EVENTOS -->
<!-- eventos temos evento de click, evento de 
  passar o mouse em cima de algo -->

<!-- Já os modificadores são utilizadas junto aos eventos
  a fim de modificar a ação de algum evento

  exemplo: prevent é um modificador que 
  impede o comportamento padrao do evento que 
  é de enviar o formulário.
  -->

<!-- 
    exemplo:
    
    SEM O MODIFICADOR

    <script setup>
import { ref } from 'vue'

function handleClick(){
console.log("cliquei")
}
</script>

<template>

<div>

<form action="https://google.com">

<button type="submit" @click="handleClick">clique
</button>


</form>


</div>

</template>


SEM O MODIFICADOR ELE VAI SUBMETER A AÇÃO DO FORMULARIO




COM O MODIFICADOR

<script setup>
import { ref } from 'vue'

function handleClick(){
console.log("cliquei")
}
</script>

<template>

<div>

<form action="https://google.com" @submit.prevent="handleClick">

<button type="submit">clique
</button>


</form>



</div>


</template>



no caso do prevent ele impede o evento padrao do evento

   -->

<!-- EXEMPLO DE PROPRIEDADE COMPUTADA -->

<!-- <script setup>
import { computed } from "vue";
import {todos} from "./Todo"



const completedTodos = computed(() => {
  return todos.filter((todo)=>todo.completed)
})

const incompletedTodos = computed(() => {
  return todos.filter((todo)=>!todo.completed)
})


</script> -->

<!-- <template>
  <h1>Todos concluidas</h1>
  <div v-for="todo in completedTodos" key="todo.id">{{ todo.title }}</div>

  <h2>Todos imcompletas</h2>
  <div v-for="todo in incompletedTodos" key="todo.id">{{ todo.title }}</div>

  <br />

  <h2>Todos</h2>

  <div v-for="todo in todos" :key="todo.id">
    <input v-model="todo.completed" type="checkbox" />
    {{ todo.title }}w
  </div>
</template> -->
