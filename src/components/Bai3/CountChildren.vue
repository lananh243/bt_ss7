<template>
  <div>
    <h3>---------- Children Component ----------</h3>

    <button @click="handleClick">Increment</button>
  </div>
</template>

<script setup>
const emit = defineEmits(["onCount"]);

const handleClick = () => {
  emit("onCount");
};
</script>

<style></style>
