<template>
  <div class="w-full py-8">
    <h3 class="text-2xl font-bold mb-8">
      {{ cardsSection.title }}
    </h3>
    <div class="w-full grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-4 gap-4">
      <SmallCard
        v-for="card in cardsSection.cards"
        :key="card.id"
        :card="card"
      />
    </div>
  </div>
</template>

<script>
export default {
  props: ["cardsSection"],
};
</script>

<style scoped></style>
