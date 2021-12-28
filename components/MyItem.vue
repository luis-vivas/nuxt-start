<template>
  <div class="flex my-12">
    <img
      :src="require(`@/assets/images/${item.image}`)"
      alt=""
      class="w-64 rounded-xl"
    />
    <div class="px-4">
      <h4 class="font-semibold text-lg">{{ item.title }}</h4>
      <p class="text-sm text-gray-500">{{ item.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ["item"],
};
</script>
