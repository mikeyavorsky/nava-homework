<script setup>
import MarketplaceHeader from "./MarketplaceHeader.vue";
import MarketplaceIntro from "./MarketplaceIntro.vue";
import MarketplaceTile from "./MarketplaceTile.vue";
import MemberForm from "./MemberForm.vue";
import RowWrap from "./RowWrap.vue";
import { ref } from "vue";

const household = ref([
  {
    name: "Bud Baxter",
    description: "Household contact",
    fruit: "Apple",
  },
  {
    name: "Andy Baxter",
    description: "Household contact",
    fruit: "Apple",
  },
]);

const handleAddMember = ({ name, description, fruit }) => {
  household.value.push({
    name,
    description,
    fruit,
  });
};
</script>

<template>
  <main>
    <MarketplaceHeader />
    <MarketplaceIntro />
    <RowWrap aria-live="polite">
      <MarketplaceTile
        v-for="member in household"
        :key="member.name"
        v-bind="member"
      />
    </RowWrap>
    <MemberForm @add-member="handleAddMember" />
  </main>
</template>

<style scoped>
main {
  overflow: visible;
}

main > :deep(*) {
  padding-left: 1rem;
  padding-right: 1rem;
}

@media (min-width: 420px) {
  main > :deep(*) {
    padding-left: 4rem;
    padding-right: initial;
  }
}
</style>
