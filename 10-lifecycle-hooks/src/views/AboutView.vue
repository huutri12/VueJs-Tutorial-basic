<template>
  <div class="about">
    <h1>Count: {{ count }}</h1>
    <button @click="increment">Increment</button>
  </div>
</template>

<script setup>
import { onBeforeUpdate, onUpdated, ref } from "vue";

const count = ref(0);

const increment = () => {
  count.value++;
};  

onBeforeUpdate(() => {
  console.log("Before Update: ", count.value);
});

onUpdated (() => {
  console.log("Updated: ", count.value);
});
</script>
