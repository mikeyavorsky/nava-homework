<script setup></script>

<template>
  <header>
    <h1><slot>Marketplace</slot></h1>
  </header>
</template>

<style scoped>
header {
  background: #25447c;
  color: white;
  width: 100%;
  min-width: min-content;
  padding: 2.5rem 4rem 1.5rem 0;
}

h1 {
  margin: 0;
  font-size: 1.75rem;
  font-weight: 800;
}
</style>
