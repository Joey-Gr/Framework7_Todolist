<template>
  <f7-page name="form">
    <f7-navbar title="Form" back-link="Back"></f7-navbar>

    <f7-block-title>Modifier un todo</f7-block-title>
    <f7-list no-hairlines-md>
      <f7-list-input v-model:value="todoName" label="Todo" type="text" placeholder="Title of your todo"></f7-list-input>
      <f7-list-input v-model:value="todoDescription" label="Description" type="text" placeholder="What is it about?"></f7-list-input>
      <f7-list-input v-model:value="todoType"  label="Type" type="text" placeholder="Type of the todo"></f7-list-input>
      <f7-list-input v-model:value="todoType"  label="Color" type="text" placeholder="Coleur du todo"></f7-list-input>
      <f7-button class="col" fill>Create</f7-button>
    </f7-list>
  </f7-page>

</template>

<script setup>
import { ref, toRefs, onMounted } from 'vue';

const todoName = ref("")
const todoDescription = ref("")
const todoType = ref("")

</script>