<script setup>
import { reactive } from 'vue';


const book = reactive({
  name: 'Book1',
  chapters: []
})

</script>

<template>
  <div>
    <p id:"count">Book name: {{ book.name }}</p>
    <p id:"count">Đã xuất bản: {{ book.chapters.length > 0 ? 'Có' : 'Không'}}</p>

  </div>
</template>
