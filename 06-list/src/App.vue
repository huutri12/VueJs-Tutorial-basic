<script setup>
import { reactive, ref } from 'vue'

const newTodo = ref('  ')

const todos = reactive([
  {
    id: 1,
    text: 'Learn VueJs ',
  },
  {
    id: 2,
    text: 'Learn Python ',
  },
  {
    id: 3,
    text: 'Learn Java ',
  },
])

const addTodo = () => {
  if (newTodo.value.trim() === '') return
  const todo = {
    id: todos.length + 1,
    text: newTodo.value,
  }
  todos.push(todo)
  newTodo.value = ''
}
</script>

<template>
  <div>
    <input type="text" v-model="newTodo" @keyup.enter="addTodo"/>
    <button @click="addTodo">Add todo</button>
    <ul>
      <li v-for="todo in todos" :key="todo.id">
        {{ todo.text }}
      </li>
    </ul>
  </div>
</template>
