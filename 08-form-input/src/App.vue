<script setup>
import { ref } from 'vue'
const text = ref('hello')
const multilineText = ref('')

const checkedName = ref([])
const radioCheck = ref('')
const selected = ref('')
const checked = ref()
</script>
<template>
  <div>
    <h1>Form input binding</h1>
    <p>Text: {{ text }}</p>
    <input v-model.lazy="text" />
    <p>Multiline Text: {{ multilineText }}</p>

    <textarea v-model="multilineText" placeholder="Input your massage" />

    <p>checkbox: {{ checked }}</p>
    <input type="checkbox" id="a" v-model="checked" true-value="yes" false-value="no" value="A" />

    <p>Multiple checkbox: {{ checkedName }}</p>
    <input type="checkbox" id="a" v-model="checkedName" value="A" />
    <label for="a">A</label>
    <input type="checkbox" id="b" v-model="checkedName" value="B" />
    <label for="b">B</label>
    <input type="checkbox" id="c" v-model="checkedName" value="C" />
    <label for="c">C</label>

    <p>Radio: {{ radioCheck }}</p>
    <input type="radio" id="d" v-model="radioCheck" value="D" />
    <label for="c">D</label>
    <input type="radio" id="e" v-model="radioCheck" value="E" />
    <label for="b">E</label>

    <p>Select: {{ selected }}</p>
    <select v-model="selected">
      <option disabled value="">Please select one</option>
      <option>A</option>
      <option>B</option>
      <option>C</option>
    </select>
  </div>
</template>
