<template>
  <div class="max-w-6xl w-full px-4 lg:px-0 lg:mx-auto">
    <LargeCardDisplay
      v-for="cardInfo in largeCardInfo.slice(0, 1)"
      :key="cardInfo.id"
      :cardsSection="cardInfo"
    />
    <SmallCardDisplay
      v-for="cardInfo in smallCardSections"
      :key="cardInfo.id"
      :cardsSection="cardInfo"
    />
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from "@/assets/data.js";
export default {
  data() {
    return {
      largeCardInfo: largeCardSections,
      smallCardSections,
    };
  },
};
</script>

<style scoped></style>
