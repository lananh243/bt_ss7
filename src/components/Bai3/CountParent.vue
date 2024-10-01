<template>
  <div>
    <h3>---------- Parent Component ----------</h3>
    <p>Count : {{count}}</p>

    <CountChildren @onCount="handleCount"/>
  </div>
</template>

<script setup>
import { ref } from "vue";
import CountChildren from "./CountChildren.vue";
const count = ref(0);

const handleCount = () => {
  count.value++;
};
</script>

<style>
</style>