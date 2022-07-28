<template>
  <div class="">
    <div
      class="py-2 px-2 sm:py-2 sm:px-8 lg:px-16 flex fixed justify-between items-center top-0 left-0 right-0 z-50 bg-[#FCF8F3]"
    >
      <div class="hidden md:flex md:pr-4 md:space-x-6 items-center">
        <a href="#" class="hover:text-gray-500 font-extrabold text-gray-900 text-xl">Funiro.</a>
        <DropdownComp class="" title="Products" :products="products" />
        <DropdownComp title="Rooms" :products="rooms" />
        <a href="#" class="font-medium text-gray-500 hover:text-gray-900">Inspirations</a>
        <SearchComp />
      </div>
      <div class="flex items-center gap-8">
        <a href="#">
          <img :src="Heart" />
        </a>
        <a href="#">
          <img :src="Cart" />
        </a>
        <a href="#">
          <img :src="Ellipse" />
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import DropdownComp from "./HeaderComponents/DropdownComponent.vue";
import SearchComp from "./HeaderComponents/SearchComp.vue";
import Heart from "../assets/Heart.svg";
import Cart from "../assets/Cart.svg";
import Ellipse from "../assets/Ellipse 2 (2).png";

export default {
  name: "Header",
  data() {
    return {
      products: ["arts", "designers", "decorations"],
      rooms: ["All rooms", "Kitchen", "Dinners", "Living", "showing"],
      Heart: Heart,
      Cart: Cart,
      Ellipse: Ellipse,
    };
  },
  components: {
    DropdownComp,
    SearchComp,
  },
};
</script>

<style></style>
