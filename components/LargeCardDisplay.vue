<template>
  <div class="w-full my-12">
    <h4 class="text-3xl font-bold">
      {{ cardsSection.title }}
    </h4>
    <p class="text-gray-500 mb-6">
      {{ cardsSection.snippet }}
    </p>
    <div class="flex flex-col lg:flex-row space-y-8 lg:space-y-0 lg:space-x-8">
      <LargeCard
        v-for="card in cardsSection.cards"
        :key="card.image"
        :card="card"
      />
    </div>
  </div>
</template>

<script>
export default { props: ["cardsSection"] };
</script>

<style lang="scss" scoped></style>
