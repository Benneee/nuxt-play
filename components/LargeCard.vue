<template>
  <div class="card">
    <img
      :src="require(`@/static/assets/images/${card.image || card.image}`)"
      :alt="card.title"
      class="image"
    />
    <h3 class="header">
      {{ card.title }}
    </h3>
    <p class="snippet">
      {{ card.snippet }}
    </p>
  </div>
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

<style scoped>
.card {
  width: 31.5%;
  height: 25rem;
  border: none;
  overflow: hidden;
  padding: 0;
  cursor: pointer;
}
.image {
  height: 65%;
  border-radius: 0.5rem;
}
.header {
  font-size: 1.15rem;
  margin-top: 0.4rem;
}
.snippet {
  color: grey;
}
</style>
