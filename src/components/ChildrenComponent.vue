<template>
  <div>
    <h1>Children Component</h1>
    <!-- B3 : Lấy giá trị từ props và render dữ liệu -->
    <h3>Ho va ten cua component con : {{userNameProps}}</h3>
    <h3>Tuổi : {{ageProps}}</h3>
    <div>
      <ul>
        <li>{{userInfoProps.name}}</li>
        <li>{{userInfoProps.age}}</li>
      </ul>
    </div>
  </div>
</template>

<script setup>
// B1 : Dinh nghia props ben tron Componet con
// const props = defineProps(["userNameProps", "ageProps"]);
const { userNameProps, ageProps } = defineProps([
  "userNameProps",
  "ageProps",
  "userInfoProps"
]);
</script>

<style>
</style>