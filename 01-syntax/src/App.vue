<script setup>
const message = ' hello world'
const rawHtml = '<span style="color: red">This should be red.</span>'
const buttonId = 'button-id'
const buttonClass = 'btn btn-rounded'
const isButtonDisabled = true
const objectOfAttrs = {
  id: 'container',
  class: 'wrapper'
}
const number = 1
const listString = 'a,b,c,d,e,f,j'
const attributeName = 'href'
const url = 'https:kungfutech.edu.vn'
</script>

<template>
  <h1>Syntax</h1>
  <p>Message: {{ message }}</p>
  <span v-html="rawHtml"></span>
  <button :id="buttonId" :class="buttonClass" :disabled="isButtonDisabled">Click here</button>
  <button v-bind="objectOfAttrs">Click Here !!!</button>
  <button :id="listString">Number: {{ number }}</button>
  <a v-bind:[attributeName]="url">Click Here</a>
</template>
