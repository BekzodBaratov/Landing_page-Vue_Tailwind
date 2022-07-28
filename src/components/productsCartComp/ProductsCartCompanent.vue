<template>
  <div class="max-w-2xl mx-auto py-16 px-4 sm:py-24 sm:px-6 lg:max-w-7xl lg:px-8">
    <h2 class="sr-only">Products</h2>
    <div class="grid grid-cols-1 gap-y-10 sm:grid-cols-2 gap-x-6 lg:grid-cols-3 xl:grid-cols-4 xl:gap-x-8">
      <a
        v-for="product in products"
        :key="product.id"
        :href="product.href"
        class="grouphref bg-gray-200 transition-all relative"
      >
        <div class="w-full aspect-w-1 aspect-h-1 bg-gray-200 overflow-hidden xl:aspect-w-7 xl:aspect-h-8">
          <img :src="product.imageSrc" :alt="product.imageAlt" class="w-full h-full object-center object-cover" />
        </div>
        <div class="absolute top-2 right-2">
          <div class="flex gap-2">
            <p
              v-if="product.new"
              class="w-14 h-14 flex items-center justify-center text-white rounded-full bg-green-700"
            >
              {{ product.new }}
            </p>
            <p
              v-if="product.sale"
              class="w-14 h-14 flex items-center justify-center text-white rounded-full bg-orange-600"
            >
              {{ product.sale }}
            </p>
          </div>
        </div>
        <div class="hoverEffect transition-all absolute top-0 left-0 bottom-0 right-0 bg-black opacity-75">
          <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2">
            <div>
              <button
                class="w-[5rem] sm:w-[7rem] md:w-[12rem] py-4 px-10 bg-white border-2 border-[#E89F71] hover:bg-[#E89F71] hover:border[#E89F71] hover:text-white opacity-100"
              >
                Add to cart
              </button>
            </div>
            <div class="flex justify-between mt-6">
              <div class="flex gap-3">
                <img :src="Share" alt="Share" />
                <p class="text-white hover:text-[#E89F71]">Share</p>
              </div>
              <div class="flex gap-3">
                <img :src="HeartWhite" alt="HeartWhite" />
                <p class="text-white hover:text-[#E89F71]">Like</p>
              </div>
            </div>
          </div>
        </div>
        <div class="px-2 pb-4">
          <h3 class="mt-4 text-2xl text-gray-900 font-medium">
            {{ product.name }}
          </h3>
          <h3 class="mt-3 text-lg font-medium text-gray-700">
            {{ product.title }}
          </h3>
          <div class="mt-4 flex justify-between items-end">
            <p class="mt-1 text-2xl font-medium text-gray-900">
              {{ product.price }}
            </p>
            <p class="mt-1 text-lg font-based text-gray-500 line-through">
              {{ product.priceReal }}
            </p>
          </div>
        </div>
      </a>
    </div>
  </div>
</template>

<script>
import HeartWhite from "../../assets/Heart_white.svg";
import Share from "../../assets/gridicons_share.svg";

import ProductCart1 from "../../assets/productsImg/image 1.png";
import ProductCart2 from "../../assets/productsImg/image 2.png";
import ProductCart3 from "../../assets/productsImg/image 3.png";
import ProductCart4 from "../../assets/productsImg/image 4.png";
import ProductCart5 from "../../assets/productsImg/Image 5.png";
import ProductCart6 from "../../assets/productsImg/image 6.png";
import ProductCart7 from "../../assets/productsImg/image 7.png";
import ProductCart8 from "../../assets/productsImg/image 8.png";

export default {
  data() {
    return {
      products: products,
      HeartWhite,
      Share,
      isTrue: false,
    };
  },
};
const products = [
  {
    id: 1,
    name: "Syltherine",
    title: "Stylish cafe chair",
    href: "#",
    new: "New",
    price: "Rp 2.500.000",
    imageSrc: ProductCart1,
    imageAlt: ProductCart1,
  },
  {
    id: 2,
    name: "Nomad Tumbler",
    href: "#",
    sale: "-50%",
    price: "Rp 1.500.000",
    priceReal: "Rp 3.000.000",
    imageSrc: ProductCart2,
    imageAlt: ProductCart2,
  },
  {
    id: 3,
    name: "Focus Paper Refill",
    href: "#",
    price: "Rp 5.500.000",
    imageSrc: ProductCart3,
    imageAlt: ProductCart3,
  },
  {
    id: 4,
    name: "Machined Mechanical Pencil",
    href: "#",
    sale: "-20%",
    price: "Rp 5.500.000",
    priceReal: "Rp 6.500.000",
    imageSrc: ProductCart4,
    imageAlt: ProductCart4,
  },
  {
    id: 5,
    name: "Machined Mechanical Pencil",
    href: "#",
    sale: "-40%",
    price: "Rp 3.500.000",
    priceReal: "Rp 6.500.000",
    imageSrc: ProductCart5,
    imageAlt: ProductCart5,
  },
  {
    id: 6,
    name: "Machined Mechanical Pencil",
    href: "#",
    new: "New",
    price: "Rp 9.500.000",
    imageSrc: ProductCart6,
    imageAlt: ProductCart6,
  },
  {
    id: 7,
    name: "Machined Mechanical Pencil",
    href: "#",
    price: "Rp 3.500.000",
    imageSrc: ProductCart7,
    imageAlt: ProductCart7,
  },
  {
    id: 8,
    name: "Machined Mechanical Pencil",
    href: "#",
    price: "Rp 5.500.000",
    imageSrc: ProductCart8,
    imageAlt: ProductCart8,
  },
  // More products...
];
</script>

<style>
.hoverEffect {
  display: none;
}
.grouphref:hover .hoverEffect {
  display: block;
}
</style>
