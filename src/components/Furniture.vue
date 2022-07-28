<template>
  <h1 class="text-gray-600 my-4 text-center">Share your setup with</h1>
  <h1 class="text-3xl font-bold mb-2 text-center">#FuniroFurniture</h1>
  <div class="gallery grid grid-cols-15 grid-rows-9 grid-flow-col gap-4">
    <img class="col-start-1 col-span-3 row-start-1 row-span-4" :src="furniture6" alt="furnitures_img" />
    <img class="col-start-1 col-span-4 row-start-5 row-span-4" :src="furniture7" alt="furnitures_img" />
    <img class="col-start-4 col-span-4 row-start-2 row-span-3" :src="furniture8" alt="furnitures_img" />
    <img class="col-start-5 col-span-3 row-start-5 row-span-3" :src="furniture9" alt="furnitures_img" />
    <img class="col-start-8 col-span-3 row-start-3 row-span-4" :src="furniture0" alt="furnitures_img40" />
    <img class="col-start-11 col-span-2 row-start-6 row-span-3" :src="furniture1" alt="furnitures_img" />
    <img class="col-start-11 col-span-3 row-start-2 row-span-4" :src="furniture3" alt="furnitures_img" />
    <img class="col-start-13 col-span-2 row-start-6 row-span-2" :src="furniture4" alt="furnitures_img" />
    <img class="col-start-14 col-span-5 row-start-1 row-span-5" :src="furniture5" alt="furnitures_img" />
  </div>
</template>

<script>
import furniture6 from "../assets/furniture/Rectangle 36.png";
import furniture7 from "../assets/furniture/Rectangle 37.png";
import furniture8 from "../assets/furniture/Rectangle 38.png";
import furniture9 from "../assets/furniture/Rectangle 39.png";
import furniture0 from "../assets/furniture/Rectangle 40.png";
import furniture1 from "../assets/furniture/Rectangle 41.png";
import furniture3 from "../assets/furniture/Rectangle 43.png";
import furniture4 from "../assets/furniture/Rectangle 44.png";
import furniture5 from "../assets/furniture/Rectangle 45.png";

export default {
  name: "Furniture",
  data() {
    return {
      furniture6: furniture6,
      furniture7: furniture7,
      furniture8: furniture8,
      furniture9: furniture9,
      furniture0: furniture0,
      furniture1: furniture1,
      furniture3: furniture3,
      furniture4: furniture4,
      furniture5: furniture5,
    };
  },
};
</script>

<style scoped>
.gallery {
  grid-auto-rows: 40px;
  grid-auto-flow: dense;
}
.gallery img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center;
}
</style>
