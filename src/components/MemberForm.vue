<script setup>
import { ref } from "vue";
import MarketplaceButton from "./MarketplaceButton.vue";

const showForm = ref(false);
const name = ref("");
const description = ref("");
const fruit = ref("");

const emit = defineEmits(["add-member"]);

const handleShowForm = () => {
  showForm.value = true;
};

const clearAndHideForm = () => {
  name.value = "";
  description.value = "";
  fruit.value = "";
  showForm.value = false;
};

const handleAdd = () => {
  emit("add-member", {
    name: name.value,
    description: description.value,
    fruit: fruit.value,
  });
  clearAndHideForm();
};
</script>

<template>
  <div class="member-form">
    <template v-if="!showForm">
      <div>
        <MarketplaceButton @click="handleShowForm" />
      </div>
    </template>
    <template v-else>
      <form @submit.prevent="handleAdd">
        <div class="form-field">
          <label for="name">Name:</label>
          <input id="name" v-model="name" type="text" />
        </div>
        <div class="form-field">
          <label for="description">Description:</label>
          <input id="description" v-model="description" type="text" />
        </div>
        <div class="form-field">
          <label for="favoriteFruit">Favorite Fruit:</label>
          <input id="favoriteFruit" v-model="fruit" type="text" />
        </div>
        <div class="button-group">
          <MarketplaceButton type="submit">Add</MarketplaceButton>
          <MarketplaceButton class="secondary" @click="clearAndHideForm">
            Cancel
          </MarketplaceButton>
        </div>
      </form>
    </template>
  </div>
</template>

<style scoped>
.member-form {
  display: flex;
  flex-direction: column;
  margin-top: 1rem;
}

form {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  padding-right: 1rem;
}

.form-field {
  display: flex;
  flex-direction: column;
  gap: 0.25rem;
  max-width: min(30rem, 90%);
}

.form-field label {
  font-weight: bold;
}

.form-field input {
  padding: 0.5rem;
  border: 1px solid #ccc;
  border-radius: 4px;
}

.form-field input:focus {
  border-color: #265d9d;
}

.button-group {
  display: flex;
  gap: 0.5rem;
  margin-top: 0.5rem;
}
</style>
