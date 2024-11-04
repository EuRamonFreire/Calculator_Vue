<template>
    <h1 class="title">App Calculadora com VueJS</h1>
    <div class="display">
      {{ value }}
    </div>
  </template>
  
  <script>
  export default {
    name: 'Display',
    props: ['value']
  }
  </script>
  
  <style scoped>
.title {
    font-size: 23px;
}
  .display {
    font-size: 2em;
    padding: 20px;
    background: #f0f0f0;
    text-align: right;
    border: 2px solid #ccc;
    border-radius: 5px;
    margin-bottom: 10px;
    box-shadow: inset 0 0 10px #0000001a;
  }
  </style>
  