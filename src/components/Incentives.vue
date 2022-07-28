<template>
  <div class="max-w-2xl mx-auto py-16 px-2 sm:py-24 sm:px-4 lg:max-w-7xl lg:px-6">
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-20 my-4 py-4">
      <div class="flex gap-4">
        <img :src="Trophy" alt="Trophy" />
        <div>
          <h3 class="line-height-150 font-semibold text-lg">High Quality</h3>
          <p class="text-[#898989]">crafted from top materials</p>
        </div>
      </div>
      <div class="flex gap-4">
        <img :src="Guarantee" alt="Guarantee" />
        <div>
          <h3 class="line-height-150 font-semibold text-lg">Warrany Protection</h3>
          <p class="text-[#898989]">Over 2 years</p>
        </div>
      </div>
      <div class="flex gap-4">
        <img :src="Shipping" alt="Shipping" />
        <div>
          <h3 class="line-height-150 font-semibold text-lg">Free Shipping</h3>
          <p class="text-[#898989]">Order over 150 $</p>
        </div>
      </div>
      <div class="flex gap-4">
        <img :src="CustomerSupport" alt="CustomerSupport" />
        <div>
          <h3 class="line-height-150 font-semibold text-lg">24 / 7 Support</h3>
          <p class="text-[#898989]">Dedicated support</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Trophy from "../assets/trophy 1.svg";
import Guarantee from "../assets/guarantee.svg";
import Shipping from "../assets/shipping.svg";
import CustomerSupport from "../assets/customer-support.svg";

export default {
  data() {
    return {
      Trophy: Trophy,
      Guarantee: Guarantee,
      Shipping: Shipping,
      CustomerSupport: CustomerSupport,
    };
  },
};
</script>

<style></style>
