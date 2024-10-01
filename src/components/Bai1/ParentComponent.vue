<template>
  <div>
    <h3>---------- Parent Component ----------</h3>
    <p>Parent Component : {{company}}</p>
    <ChildrenComponent :companyProps="company"></ChildrenComponent>
  </div>
</template>

<script setup>
import ChildrenComponent from "../Bai1/ChildrenComponent.vue";
const company = "Rikkei Academy";
</script>

<style>
</style>