<template>
  <MessageChildren @onChange="handleAlert" />
</template>

<script setup>
import MessageChildren from "./MessageChildren.vue";
const handleAlert = () => {
  alert("Welcome to Rikkei Education");
};
</script>

<style></style>
