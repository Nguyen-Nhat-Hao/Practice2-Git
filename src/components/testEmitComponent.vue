<template>
  <div>
    <button @click="buttonClicked">Click me!</button>
    <p>abc</p>
    <div>
      <p> what your name ?</p>
    </div>
  </div>
  </template>
  
  <script>
  export default {
    methods: {
      buttonClicked() {
        // Phát ra sự kiện 'button-clicked' với thông tin dữ liệu 'Hello, world!'
        this.$emit('button-clicked', 'Hello, world!');
      }
    }
  }
  </script>
  <style lang="scss" scoped>
  
  </style>