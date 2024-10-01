<template>
  <div>
    <h3>------------TodoApp Component ------------</h3>
    <p>Id to delete : {{remove}}</p>

    <TodoItem @onClick="handleClick"></TodoItem>
  </div>
</template>

<script setup>
import TodoItem from "./TodoItem.vue"
import { ref } from "vue";

const remove = ref(0);
const handleClick = () => {
    remove.value ++;
}


</script>

<style>

</style>