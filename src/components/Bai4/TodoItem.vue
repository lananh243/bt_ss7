<template>
  <div>
    <h3>-------------- TodoItem Component -----------------</h3>
    <button @click="handleCount">Delete</button>
  </div>
</template>

<script setup>
const emit = defineEmits(["onClick"]);
const handleCount = () => {
    emit("onClick")
}
</script>

<style>

</style>