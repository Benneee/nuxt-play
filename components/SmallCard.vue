<template>
  <NuxtLink :to="`/products/${card.id}`" class="card">
    <img
      class="image"
      :src="require(`@/static/assets/images/${card.image || card.image}`)"
      :alt="card.id"
    />
  </NuxtLink>
</template>

<script>
export default {
  props: {
    card: {
      type: Object,
      required: true
    }
  }
};
</script>

<style>
.card {
  width: 24%;
  height: 12.5rem;
  border-radius: 0.5rem;
  overflow: hidden;
  margin-bottom: 1.5rem;
  cursor: pointer;
}
.image {
  width: 100%;
  height: 100%;
}
</style>
