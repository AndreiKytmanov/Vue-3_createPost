<template>
  <button class="add__post-btn">
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: "my-button"
};
</script>

<style scoped>
.add__post-btn {
  padding: 10px;
  background-color: transparent;
  border: 2px solid teal;
  cursor: pointer;
  color: teal;
  transition: all 0.3s ease-in;
}

.add__post-btn:hover {
  background-color: #637d7d;
  color: #fff;
}
</style>
