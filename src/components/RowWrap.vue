<script setup></script>

<template>
  <div class="row-wrap"><slot /></div>
</template>

<style scoped>
.row-wrap {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
}
</style>
