<template>
  <div class="grid bg-[#FCF8F3] my-6" style="grid-template-columns: 4fr 6fr">
    <div class="p-20 flex flex-col justify-center">
      <h2 class="text-3xl font-bold mb-3">50+ Beautiful rooms inspiration</h2>
      <p class="text-gray-600 mb-3">Our designer already made a lot of beautiful prototipe of rooms that inspire you</p>
      <button
        class="w-40 bg-[#E89F71] border-2 transition-all border-[#E89F71] py-2 text-white hover:bg-white hover:text-[#E89F71] focus:bg-white focus:text-[#E89F71]"
      >
        Explore More
      </button>
    </div>
    <div class="relative overflow-hidden py-6">
      <div
        class="flex items-start gap-4 w-[200vw] transition-all"
        :style="'transform:translate(-' + imgCount * 25 + 'rem)'"
      >
        <div
          v-for="(room, index) in rooms"
          :key="index"
          class="relative bg-slate-400 transition-all"
          :class="index === this.imgCount ? 'h-[80vh] w-[17%]' : 'h-[70vh] w-[14%]'"
        >
          <img class="w-full" :src="room.img" alt="rooms" />
          <div class="absolute bottom-4 left-4">
            <div
              class="relative py-8 px-6 translate-x-10 transition-all duration-300"
              :class="this.imgCount == index ? 'visible' : 'invisible'"
            >
              <div class="relative z-10">
                <p class="text-gray-600 text-sm">{{ room.room }}</p>
                <p class="text-xl font-normal">{{ room.desc }}</p>
              </div>
              <button
                class="absolute left-full bottom-0 py-2 px-4 text-white bg-[#E89F71] transition-all hover:left-[105%]"
              >
                &rarr;
              </button>
              <div class="absolute inset-0 bg-white opacity-70"></div>
            </div>
          </div>
        </div>
      </div>
      <div>
        <span @click="next" class="text-white absolute right-5 top-1/2">
          <div
            class="flex items-center justify-center w-8 h-8 bg-[#E89F71] rounded-full transition-all hover:translate-x-1"
          >
            <p>
              <svg
                class="h-6 w-6 -rotate-90"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 20 20"
                fill="currentColor"
                aria-hidden="true"
              >
                <path
                  fill-rule="evenodd"
                  d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
                  clip-rule="evenodd"
                ></path>
              </svg>
            </p>
          </div>
        </span>
        <div class="absolute bottom-2 left-[59%] kallaUxshamadi flex gap-4">
          <span
            class="w-3 h-3 rounded-full bg-orange-600"
            v-for="(n, key) in rooms.length - 1"
            :class="key == imgCount ? 'outline outline-offset-4 outline-1 outline-orange-600' : ''"
            :key="key"
          ></span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import room1 from "../assets/rooms/Rectangle 24.png";
import room2 from "../assets/rooms/Rectangle 25.png";
import room3 from "../assets/rooms/Rectangle 26.png";

export default {
  data() {
    return {
      rooms: [
        { img: room1, room: "01 -- Bad Room", desc: "Inner Peace", href: "#" },
        { img: room2, room: "02 -- Leaving Room", desc: "Inner Peace", href: "#" },
        { img: room3, room: "03 -- Citchen", desc: "Inner Peace", href: "#" },
        { img: room2, room: "04 -- Show Room", desc: "Inner Peace", href: "#" },
        { img: room3, room: "05 -- Bad Room", desc: "Inner Peace", href: "#" },
      ],
      imgCount: 0,
    };
  },
  methods: {
    next() {
      if (this.imgCount < this.rooms.length - 2) {
        this.imgCount++;
      } else {
        this.imgCount = 0;
      }
    },
  },
};
</script>

<style></style>
