<template>
  <button @click="handldChange">Send message</button>
</template>

<script setup>
const emit = defineEmits(["onChange"]);

const handldChange = () => {
  emit("onChange");
};
</script>

<style></style>
