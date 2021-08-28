<template>
  <div class="container">
    <MyItem
      v-for="rental in myRentals"
      :key="`rental-${rental.id}`"
      :item="rental"
      @removeItemFromList="removeItemFromMyItems($event)"
    />
  </div>
</template>

<script>
import { mapState, mapMutations } from "vuex";
export default {
  layout: "no-nav",

  computed: {
    ...mapState(["myRentals"])
  },

  methods: {
    ...mapMutations(["removeItem"]),

    removeItemFromMyItems(item) {
      this.removeItem(item.id);
    }
  }
};
</script>

<style></style>
