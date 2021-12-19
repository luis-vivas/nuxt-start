<template>
  <div class="flex-1 overflow-hidden cursor-pointer">
    <img
      class="h-4/6 rounded-xl w-full mb-4"
      :src="require(`@/assets/images/${card.image || 'fe1.jpg'}`)"
      alt=""
    />
    <h3 class="text-lg font-medium mb-2">{{ card.title }}</h3>
    <p class="text-gray-500 mb-4">
      {{ card.snippet }}
    </p>
  </div>
</template>

<script>
export default { props: ["card"] };
</script>

<style lang="scss" scoped></style>
