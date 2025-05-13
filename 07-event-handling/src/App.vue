<script setup>
import { ref } from 'vue'
const sayHi1 = () => {
  alert(`xin chao 1`)
}
const sayHi2 = () => {
  alert(`xin chao 2`)
}

const submit = () => {
  alert(' Form submited ')
}
</script>

<template>
  <div>
    <h1>Event Handing</h1>
    <!-- <button @click="sayHi1">
      <button @click.stop="sayHi2">say hi 2</button>
      say hi 1
    </button> -->
    <form @submit.prevent="submit">
      <button type="submit">Submit</button>
    </form>
    <br />
    <input @keyup.enter.alt="submit" placeholder="nhập tên của bạn" />
    <button @click.shift="submit">Submit</button>
  </div>
</template>
