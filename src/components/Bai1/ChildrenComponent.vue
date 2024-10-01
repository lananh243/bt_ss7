<template>
  <div>
    <h3>---------- Children Component ----------</h3>
    <p>ChildrenComponent : {{companyProps}}</p>
  </div>
</template>

<script setup>
const props = defineProps(["companyProps"]);
</script>

<style>
</style>