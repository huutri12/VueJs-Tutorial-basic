<script setup>
import { computed, reactive } from 'vue'

const book = reactive({
  name: 'Book1',
  chapters: [],
})

const addChapter = () => {
  book.chapters.push('Chapter')
}

const isPublished = computed(() => {
  return book.chapters.length > 0 ? 'Có' : 'Không'
})
</script>

<template>
  <div>
    <p>Book name: {{ book.name }}</p>
    <p>Đã xuất bản: {{ isPublished }}</p>
    <button @click="addChapter">Add Chapter</button>
  </div>
</template>
