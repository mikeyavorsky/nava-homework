<script setup>
import { ref } from "vue";

defineProps({
  msg: String,
});

const count = ref(0);
</script>

<template>
  <h2>Your household</h2>
  <p>Welcome to The Marketplace! Review your household below:</p>
</template>

<style scoped>
h2 {
  font-size: 1.5rem;
  font-weight: 800;
}
</style>
