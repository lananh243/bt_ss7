<template>
  <div class="overlay" @click="handleCloseForm">
    <div class="form-container">
      <h2>Form Add User</h2>
      <form>
        <div class="form-group">
          <label for="name">Name</label>
          <input type="text" id="name" name="name" />
        </div>
        <div class="form-group">
          <label for="email">Email</label>
          <input type="email" id="email" name="email" />
        </div>
        <div class="form-group">
          <label for="address">Address</label>
          <input type="text" id="address" name="address" />
        </div>
        <button type="button" class="btn-close" @click="handleCloseForm">
          Close
        </button>
      </form>
    </div>
  </div>
</template>
<script setup>
const emit = defineEmits();
const handleCloseForm = () => {
  emit("closeForm");
};
</script>
<style scoped>
.overlay {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: center;
  align-items: center;
}

.form-container {
  width: 300px;
  padding: 20px;
  border-radius: 10px;
  background-color: white;
  text-align: center;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
}

.form-group {
  margin-bottom: 15px;
  text-align: left;
}

.form-group input {
  width: 285px;
  padding: 8px;
  border: 1px solid #ccc;
  border-radius: 5px;
}

.btn-close {
  background-color: red;
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 5px;
  cursor: pointer;
}
</style>
