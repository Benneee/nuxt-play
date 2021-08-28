<template>
  <div>
    <h3>Customer Reviews</h3>
    <p v-if="$fetchState.pending">Loading reviews....</p>
    <p v-else-if="$fetchState.error">An error occurred</p>
    <div v-else>
      <ReviewCard
        v-for="reviewer in reviewers.results"
        :key="`reviewer-${reviewer.login.uuid}`"
        :review="reviewer"
      />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      reviewers: []
    };
  },

  async fetch() {
    this.reviewers = await fetch(
      "https://randomuser.me/api/?results=5"
    ).then(res => res.json());
  }
};
</script>

<style></style>
