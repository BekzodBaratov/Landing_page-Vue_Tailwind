<template>
  <div class="overflow-x-hidden">
    <Hero />
    <Incentives />
    <ProductsCart />
    <Rooms />
    <Tips />
    <Furnitures />
    <Footer />
  </div>
</template>

<script>
import Hero from "./components/Hero.vue";
import Incentives from "./components/Incentives.vue";
import ProductsCart from "./components/ProductsCart.vue";
import Rooms from "./components/RoomsSlider.vue";
import Tips from "./components/Tips.vue";
import Footer from "./components/Footer.vue";
import Furnitures from "./components/Furniture.vue";

export default {
  name: "App",
  components: {
    Hero,
    Incentives,
    ProductsCart,
    Rooms,
    Tips,
    Furnitures,
    Footer,
  },
};
</script>

<style></style>
