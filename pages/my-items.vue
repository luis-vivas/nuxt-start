<template>
  <div class="max-w-4xl w-full px-4 lg:px-0 lg:mx-auto py-8">
    <MyItem v-for="rental in myRentals" :key="rental.id" :item="rental" />
  </div>
</template>

<script>
import { mapState } from "vuex";
export default {
  layout: "no-nav",
  computed: {
    ...mapState(["myRentals"]),
  },
};
</script>
