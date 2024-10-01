<template>
  <ProductChildren :productProps="product" />
</template>

<script setup>
import ProductChildren from "../Bai2/ProductChildren.vue";
const product = {
  id: 1,
  name: "Bưởi Ba Roi",
  price: "12.000 đ",
  quantity: 10
};
</script>

<style>
</style>