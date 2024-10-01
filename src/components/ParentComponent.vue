<template>
  <div>
    <h1>Parent Component</h1>
    <!-- Sử dụng component con -->
    <!-- B2 : Trong component cha gọi props đc khai báo bên con và truyền giá trị -->
    <ChildrenComponent userNameProps="Lan Anh" :ageProps="age" :userInfoProps="userInfo" />
    <h3>Ten nguoi dung : {{user}}</h3>
  </div>
</template>

<script setup>
import ChildrenComponent from "./ChildrenComponent.vue";
const user = "Lan Anh";

const age = 19;

const userInfo = {
  id: 1,
  name: "Nguyễn Văn B",
  age: 21
};
</script>

<style>
</style>