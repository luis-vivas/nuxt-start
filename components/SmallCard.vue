<template>
  <div class="h-48 rounded-xl overflow-hidden cursor-pointer">
    <img
      :src="require(`@/assets/images/${card.image || 'fe1.jpg'}`)"
      alt="fe"
      class="w-full h-full"
    />
  </div>
</template>

<script>
export default {
  props: ["card"],
};
</script>

<style scoped></style>
