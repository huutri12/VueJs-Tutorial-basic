<script setup>
import { ref, reactive } from 'vue'
const isLoggedIn = ref(true)
const toggleLogin = () => {
  isLoggedIn.value = !isLoggedIn
}

const isVisible = ref(true)
const toggleShow = () => {
  isVisible.value = !isVisible
}

const userStatus = ref('busy')

const changeStatus = () => {
  if (userStatus.value === 'online') {
    userStatus.value = 'away'
  } else if (userStatus.value === 'alway') {
    userStatus.value = 'busy'
  } else if (userStatus.value === 'busy') {
    userStatus.value = 'online'
  }
}
</script>

<template>
  <div>
    <h1 v-if="isLoggedIn">Chào mừng người dùng đã đăng nhập</h1>
    <h1 v-else>Chào mừng khách</h1>
    <button @click="toggleLogin">{{ isLoggedIn ? 'Đăng xuất' : 'Đăng nhập' }}</button>
    <br />
    <h1 v-if="userStatus === 'online'">Người dùng đang online</h1>
    <h1 v-else-if="userStatus === 'alway'">Người dùng đang vắng mặt</h1>
    <h1 v-else-if="userStatus === 'busy'">Người dùng đang bận</h1>
    <h1 v-else>Không rõ trạng thái</h1>
    <button @click="changeStatus">Thay đổi trạng thái</button>
    <br />
    <h1 v-show="isVisible">Nội dung ẩn hoặc hiển thị</h1>
    <button @click="toggleShow">{{ isVisible ? 'Ẩn' : 'Hiện' }}</button>
  </div>
</template>
