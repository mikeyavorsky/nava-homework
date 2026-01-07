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
    <RowWrap>
      <h3>{{ props.name }}</h3>
    </RowWrap>
    <RowWrap><strong>Description:</strong> {{ props.description }}</RowWrap>
    <RowWrap><strong>Favorite fruit:</strong> {{ props.fruit }}</RowWrap>
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
  margin: 0 0 1rem 0;
}

strong {
  margin: 0 0.25rem 0.5rem 0;
}
</style>
