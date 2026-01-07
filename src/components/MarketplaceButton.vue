<script setup></script>

<template>
  <button><slot>Add new member</slot></button>
</template>

<style scoped>
button {
  background-color: #265d9d;
  color: white;
  font-weight: bold;
}

button:hover {
  background-color: #1e4a7a;
}

.secondary {
  background-color: #6c757d;
  color: white;
}

.secondary:hover {
  background-color: #5a6268;
}
</style>
