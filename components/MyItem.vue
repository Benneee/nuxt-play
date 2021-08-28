<template>
  <div class="item-container">
    <img :src="require(`@/static/assets/images/${item.image}`)" alt="" />
    <div class="text-container">
      <div class="description-container">
        <h4>{{ item.title }}</h4>
        <button class="btn btn-sm btn-danger" @click="removeItem(item)">
          Remove
        </button>
      </div>

      <p>{{ item.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    item: {
      type: Object,
      required: true
    }
  },

  methods: {
    removeItem(product) {
      this.$emit("removeItemFromList", product);
    }
  }
};
</script>

<style scoped>
.item-container {
  display: flex;
  margin: 3rem 0;
}
.text-container {
  padding: 0 1rem;
}
.description-container {
  display: flex;
  justify-content: space-between;
}
img {
  width: 17.5rem;
  border-radius: 0.5rem;
  height: 11rem;
}
p {
  font-size: 0.8rem;
  color: grey;
}
</style>
