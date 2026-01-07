<script setup>
import MarketplaceHeader from "./MarketplaceHeader.vue";
import MarketplaceIntro from "./MarketplaceIntro.vue";
import MarketplaceTile from "./MarketplaceTile.vue";
import MarketplaceButton from "./MarketplaceButton.vue";
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
</script>

<template>
  <main>
    <MarketplaceHeader />
    <MarketplaceIntro />
    <RowWrap>
      <MarketplaceTile
        v-for="member in household"
        :key="member.name"
        v-bind="member"
      />
    </RowWrap>
    <MarketplaceActions />
    <div><MarketplaceButton> </MarketplaceButton></div>
  </main>
</template>

<style scoped>
main {
  overflow: visible;
}

main > :deep(*) {
  padding-left: 4rem;
}
</style>
