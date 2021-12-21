<template>
  <div>
    <Nav />
    <div class="max-w-6xl w-full px-4 lg:px-0 lg:mx-auto">
      <div v-if="product" class="py-12">
        <div class="flex space-x-8">
          <img
            :src="require(`@/assets/images/${product.image}`)"
            alt=""
            class="h-96 w-1/2 rounded-xl"
          />
          <div class="w-2/5 bg-gray-200 p-4 rounded-xl">
            <h1 class="text-2xl">{{ product.title }}</h1>
            <p class="text-black/[.7] my-4">{{ product.snippet }}</p>
            <button
              class="w-full text-lg text-white font-semibold px-12 p-4 mb-8 rounded-full bg-red-400 transition-all duration-500 ease-in-out hover:px-16"
            >
              Rent
            </button>
            <!-- <RentModal :product="product" /> -->
          </div>
        </div>
        <div class="my-12 border-b">
          <div v-for="(title, index) in titles" :key="index" class="mb-8">
            <h6 class="text-xl font-semibold mb-2">{{ title }}</h6>
            <p class="text-gray-500">
              Lorem ipsum dolor sit amet consectetur adipisicing elit.
              Asperiores, dolorem.
            </p>
          </div>
        </div>
        <div class="border-b pb-8 mb-8">
          <p>
            {{ product.description }}
          </p>
        </div>
        <!-- <Reviews /> -->
      </div>
      <div v-else class="text-center mx-auto py-40 text-3xl">
        <!-- <PageNotFound /> -->
        Page Not Found
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      titles: [
        "Super Effective",
        "Clean & Tidy",
        "Cancel Anytime",
        "Satisfaction Guaranteed",
      ],
    };
  },
  computed: {
    product() {
      return this.$store.getters.getProductById(this.$route.params.id);
    },
  },
};
</script>

<style scoped></style>
