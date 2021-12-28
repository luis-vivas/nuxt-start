<template>
  <div class="p-4 mt-6 flex border rounded-md hover:border-red-300">
    <div class="w-14 h-14 rounded-full overflow-hidden ring ring-red-400">
      <img :src="review.picture.large" alt="" />
    </div>
    <div class="ml-8">
      <h6>{{ review.login.username }}</h6>
      <p class="text-gray-500">
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Repellendus
        quam magni beatae possimus debitis.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: ["review"],
};
</script>

<style scoped></style>
