<template>
  <div class="relative mb-10">
    <Rectangle />
    <Header />
    <carousel :slides="slides" :interval="3000" controls indicators></carousel>
    <HeroCart />
  </div>
</template>

<script>
import Header from "./Header.vue";
import Carousel from "./carousel/Carousel.vue";
import Rectangle from "./hero/Rectangle.vue";
import HeroCart from "./hero/HeroCart.vue";

export default {
  name: "Hero",
  components: {
    Header,
    Carousel,
    Rectangle,
    HeroCart,
  },
  data: () => ({
    slides: [
      "https://picsum.photos/id/1032/900/400",
      "https://picsum.photos/id/1033/900/400",
      "https://picsum.photos/id/1037/900/400",
      "https://picsum.photos/id/1035/900/400",
      "https://picsum.photos/id/1036/900/400",
    ],
  }),
};
</script>

<style></style>
