<template>
  <f7-page name="todo">
    <f7-navbar title="Todo" back-link="Back">
      <f7-button fill href="/todo/create">+</f7-button>
    </f7-navbar>
    <f7-block-title>Todos</f7-block-title>
    <f7-list>
      <f7-list-item v-for="(todo) in todos" :link="'/todo/'+todo.idTodo+'/modify'" :title="todo.todoName" checkbox value="check_1">
        <p>{{ todo.todoDesc }}</p>
      </f7-list-item>
    </f7-list>
  </f7-page>
{{ routeParam }}
</template>

<script setup>
import { ref, toRefs, onMounted } from 'vue';



const todoName = ref("")
const todoDescription = ref("")
const todoType = ref("")

const todos = ref([
  {
    "idTodo": 0,
    "todoName": "Timezone",
    "todoDesc": "Don't forget the timezones! At 4 AM",
    "todoType": ""
  },
  {
    "idTodo": 1,
    "todoName": "Trials",
    "todoDesc": "There's an important trial this afternoon",
    "todoType": ""
  },
  {
    "idTodo": 2,
    "todoName": "Game",
    "todoDesc": "There's this game I would like to play one day...",
    "todoType": ""
  }
])

</script>