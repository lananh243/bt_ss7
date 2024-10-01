<template>
  <div>
    <!-- <h1>Home Page</h1>
    <ParentComponent />
    <BaseButton></BaseButton>
    <BaseButton title="Add product"></BaseButton>-->
    <!-- <SlotComponent> -->
    <!-- Nội dung này chính là slot sau này dùng -->
    <!-- <a href>Face book</a> -->
    <!-- </SlotComponent> -->

    <!-- <BaseButton @onClick="handleClickParent">Click me</BaseButton>
    <p>*************************</p>-->
    <h1>Bài tập 1 :</h1>
    <ParentComponent />
    <h1>Bài tập 2 :</h1>
    <ProductParent />
    <h1>Bài tập 3 :</h1>
    <CountParent />
    <h1>Bài tập 4 :</h1>
    <TodoApp />
    <h1>Bài tập 5 :</h1>
    <Modal class="modal" v-if="isModal">
      <template #header>
        <div
          style="
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 430px;
          "
        >
          <h4 class="title">Thông báo từ hệ thống</h4>
          <span @click="handleClose" style="cursor: pointer; font-size: 25px"
            >&times;</span
          >
        </div>
        <hr />
      </template>

      <template #body>
        <p class="body">
          Đây là nội dung của modal. Bạn có thể đóng modal bằng cách nhấn vào
          nút 'Close'.
        </p>
        <hr />
      </template>

      <template #footer>
        <div class="footer">
          <button class="btn" @click="handleClose">Close</button>
        </div>
      </template>
    </Modal>

    <h1>Bài tập 6 :</h1>
    <Card class="modal">
      <template #header>
        <h4 class="title">Thông tin sản phẩm</h4>
        <hr />
      </template>
      <template #body>
        <p class="body">
          Đây là mô tả ngắn gọn về sản phẩm này. Sản phẩm có các tính năng nổi
          bật và giá cả hợp lý.
        </p>
        <hr />
      </template>
      <template #footer>
        <div class="detail">
          <button class="but">Xem chi tiết</button>
        </div>
      </template>
    </Card>
    <h1>Bài tập 7 :</h1>
    <MessageParent></MessageParent>
    <h1>Bài tập 8 :</h1>
    <ListUser></ListUser>
  </div>
</template>

<script setup>
// import ParentComponent from "./components/ParentComponent.vue";
// import BaseButton from "./components/BaseButton.vue";
// import SlotComponent from "./components/SlotComponent.vue";
import ParentComponent from "./components/Bai1/ParentComponent.vue";
import ProductParent from "./components/Bai2/ProductParent.vue";
import CountParent from "./components/Bai3/CountParent.vue";
import TodoApp from "./components/Bai4/TodoApp.vue";
import Card from "./components/Bai6/Card.vue";
import Modal from "./components/Bai5/Modal.vue";
import MessageParent from "./components/Bai7/MessageParent.vue";
import ListUser from "./components/Bai8/ListUser.vue";
import { ref } from "vue";
const isModal = ref(true);
const handleClose = () => {
  isModal.value = false;
};
const handleClick = () => {
  console.log("Clicked");
};

const handleClickParent = (data) => {
  console.log("Dữ liệu truyền từ con : ", data);
};
</script>

<style scoped>
.modal {
  width: 450px;
  height: 200px;
  border: 1px solid grey;
  display: flex;
  flex-direction: column;
}

.title {
  padding-left: 20px;
}

.body {
  padding-left: 20px;
}

.footer {
  display: flex;
  justify-content: right;
  padding: 10px;
}
.detail {
  padding: 20px;
}
.btn {
  padding: 5px 20px;
  cursor: pointer;
}
.but {
  padding: 6px 25px;
  background-color: rgb(127, 165, 248);
  border: none;
  color: white;
}
hr {
  width: 100%;
  margin: 0;
}
</style>
