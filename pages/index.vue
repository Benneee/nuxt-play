<template>
  <div class="container">
    <Hero />
    <LargeCardDisplay
      v-for="cardInfo in largeCardInfo"
      :key="cardInfo.id"
      :cardsSection="cardInfo"
    />
  </div>
</template>

<script>
import { largeCardSections } from "@/static/assets/data.js";
export default {
  data() {
    return {
      largeCardInfo: largeCardSections
    };
  }
};
</script>
