<script setup>
import RowWrap from "./RowWrap.vue";

const props = defineProps({
  name: String,
  description: String,
  fruit: String,
});
</script>

<template>
  <div class="flex-column tile tile-border">
    <h3>{{ props.name }}</h3>
    <span><strong>Description:</strong> {{ props.description }}</span>
    <span><strong>Favorite fruit:</strong> {{ props.fruit }}</span>
  </div>
</template>

<style scoped>
.flex-column {
  display: flex;
  flex-direction: column;
}

.tile {
  padding: 1rem;
}

.tile-border {
  border: 1px solid #ccc;
  border-radius: 8px;
}

h3 {
  font-weight: 800;
  margin: 0 0 1rem 0;
}

strong {
  font-weight: 700;
  margin: 0 0.125rem 0.5rem 0;
}

span {
  margin-bottom: 0.5rem;
}
</style>
