<template>
  <div>
    Hello from product with ID {{ $route.params.id }}
    {{ product.description }}
  </div>
</template>

<script>
import { mapState, mapGetters } from "vuex";
export default {
  computed: {
    ...mapState(["products"]),
    ...mapGetters(["getProductById"]),

    product() {
      const productId = this.$route.params.id;
      return this.getProductById(productId);
    }
  }
};
</script>

<style scoped></style>
