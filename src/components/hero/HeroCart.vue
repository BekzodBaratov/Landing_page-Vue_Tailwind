<template>
  <div class="absolute hidden md:block heroCart w-80 left-8 sm:left-16 top-20 p-10 z-10">
    <div class="absolute inset-0 bg-white backdrop-blur-sm bg-white/30 -z-10">
      <div class="absolute inset-0 bg-white opacity-70 -z-20"></div>
    </div>
    <div class="">
      <h2 class="font-bold text-2xl leading-tight mb-4">High-Quality Furniture Just For You</h2>
      <p class="line-height-2 leading-normal mb-10 text-gray-600">
        Our furniture is made from selected and best quality materials that are suitable for your dream home
      </p>
      <button
        class="relative w-full bg-orange-400 py-2 text-white transition-all border-2 border-orange-400 hover:bg-white hover:text-orange-600"
      >
        Shop Now
      </button>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.heroCart::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -10;
  opacity: 1;
  filter: brightness(0.3);
}
</style>
