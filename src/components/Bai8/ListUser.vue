<template>
  <div>
    <h3>-------------- List User ---------------</h3>
    <button @click="handleChange">Add user</button>

    <FormAddUser v-if="isShowForm" @closeForm="handleCloseForm" />
  </div>
</template>

<script setup>
import { ref } from "vue";
import FormAddUser from "./FormAddUser.vue";

const isShowForm = ref(false);

const handleChange = () => {
  isShowForm.value = true;
  console.log("Form displayed:", isShowForm.value);
};

const handleCloseForm = () => {
  isShowForm.value = false;
};
</script>

<style scoped>
button {
  background-color: rgb(127, 165, 248);
  color: white;
  height: 35px;
  width: 120px;
  border: none;
  cursor: pointer;
}
</style>
