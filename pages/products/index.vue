<template>
  <div>
    <Nav />
    <div class="container">
      <LargeCardDisplay
        v-for="cardInfo in largeCardInfo.slice(0, 1)"
        :key="`largecard-${cardInfo.id}`"
        :cardsSection="cardInfo"
      />

      <SmallCardDisplay
        v-for="cardInfo in smallCardInfo.slice(0, 1)"
        :key="`smallcard-${cardInfo.id}`"
        :cardsSection="cardInfo"
      />
    </div>
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from "@/static/assets/data.js";
export default {
  data() {
    return {
      largeCardInfo: largeCardSections,
      smallCardInfo: smallCardSections
    };
  }
};
</script>

<style></style>
