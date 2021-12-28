<template>
  <div>
    <button
      @click="showModal = true"
      class="w-full text-lg text-white font-semibold px-12 p-4 mb-8 rounded-full bg-red-400 transition-all duration-500 ease-in-out hover:px-16"
    >
      Rent
    </button>
    <div
      id="overlay"
      v-show="showModal"
      class="fixed top-0 left-0 w-screen h-screen flex justify-center content-center bg-gray-900/[.6]"
    >
      <div
        id="modal"
        class="w-2/5 my-auto p-5 rounded-xl shadow-lg bg-white space-y-4"
      >
        <div class="flex">
          <div class="p-2">
            <p class="my-4 text-gray-500">
              Lorem ipsum dolor sit amet consectetur, adipisicing elit.
              Asperiores quis soluta quia neque! Ea modi, a omnis eligendi enim
              ducimus asperiores. Lorem ipsum dolor sit amet consectetur
              adipisicing elit. Laborum, autem?
            </p>
          </div>
          <vc-date-picker :value="null" color="indigo" is-dark is-range />
        </div>
        <button
          class="w-full text-lg text-white font-semibold px-12 p-4 rounded-full bg-red-400 transition-all duration-500 ease-in-out hover:px-16"
          @click="
            () => {
              addItem(product.id);
              showModal = false;
            }
          "
        >
          Order
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import { mapMutations } from "vuex";
export default {
  data() {
    return {
      showModal: false,
    };
  },
  props: ["product"],
  methods: {
    ...mapMutations(["addItem"]),
  },
};
</script>
