<template>
  <div>
    <h3>Dữ liệu trong component con</h3>
    <p>Id : {{productProps.id}}</p>
    <p>Product name : {{productProps.name}}</p>
    <p>Price : {{productProps.price}}</p>
    <p>Quantity : {{productProps.quantity}}</p>
  </div>
</template>

<script setup>
const props = defineProps(["productProps"]);
</script>

<style>
</style>