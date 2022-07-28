<template>
  <h1 class="font-bold text-3xl text-center">Our Products</h1>
  <ProductsCartComp />
  <div class="text-center">
    <button class="py-2 px-10 border-2 border-[#E89F71] hover:bg-[#E89F71] hover:text-white">Show More</button>
  </div>
</template>

<script>
import ProductsCartComp from "./productsCartComp/ProductsCartCompanent.vue";

export default {
  components: {
    ProductsCartComp,
  },
};
</script>

<style></style>
