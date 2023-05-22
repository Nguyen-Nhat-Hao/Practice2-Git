<template>
  <div>
    <h2>Please Click Me !</h2>
    <button @click="buttonClicked">Click me!</button>
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
      this.$emit("button-clicked", "Hello, world!");
    },
  },
};
</script>
<style lang="scss" scoped></style>
