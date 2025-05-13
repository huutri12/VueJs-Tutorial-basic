<script setup>
import { ref } from 'vue'
const sayHi1 = () => {
  alert(`xin chao 1`)
}
const sayHi2 = () => {
  alert(`xin chao 2`)
}
</script>

<template>
  <div>
    <h1>Event Handing</h1>
    <button @click="sayHi1">
      <button @click.stop="sayHi2">say hi 2</button>
      say hi 1
    </button>
  </div>
</template>
