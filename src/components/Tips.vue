<template>
  <div class="mx-2 md:mx-8 lg:mx-16 overflow-hidden relative py-12">
    <h1 class="text-3xl font-bold text-center">Tips & Tricks</h1>
    <div
      class="tips flex flex-nowrap w-[150vw] gap-6 my-10 transition-all"
      :style="'transform:translate(-' + rasmSoni * 26 + 'rem)'"
    >
      <CarouselSlide v-for="(slide, index) in slides" :key="index">
        <div
          class="transition-all hover:bg-white hover:shadow-2xl min-w-1/3"
          :class="this.caruselCircle == index ? 'bg-gray-200 ' : ''"
        >
          <img class="w-auto" :src="slide.img" alt="slide" />
          <div class="p-4">
            <h1 class="mb-4 text-gray-900 text-xl font-bold">{{ slide.title }}</h1>
            <p class="text-gray-600">{{ slide.date }}</p>
          </div>
        </div>
      </CarouselSlide>
    </div>
    <button
      @click="next"
      class="absolute right-0 top-1/2 -translate-y-1/2 w-10 btnSlideN h-10 rounded-full bg-white text-orange-500 flex items-center justify-center"
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
    </button>
    <button
      @click="prev"
      class="absolute left-0 top-2/4 -translate-y-1/2 btnSlideP w-10 h-10 rounded-full bg-white text-orange-500 flex items-center justify-center"
    >
      <p>
        <svg
          class="h-6 w-6 rotate-90"
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
    </button>
    <Carousel :controlCircle="this.slides.length" :caruselCircle="this.caruselCircle"> </Carousel>
  </div>
</template>

<script>
import Carousel from "./tipsCarusel/carousel.vue";
import CarouselSlide from "./tipsCarusel/carouselSlide.vue";

export default {
  name: "Tips",
  data() {
    return {
      slides: [
        {
          img: "https://picsum.photos/id/237/600/350",
          title: "How to create a living room to love",
          date: "20 jan 2020",
        },
        {
          img: "https://picsum.photos/id/236/600/350",
          title: "Solution for clean look working space",
          date: "20 jan 2020",
        },
        {
          img: "https://picsum.photos/id/235/600/350",
          title: "Make your cooking activity more fun with good setup",
          date: "20 jan 2020",
        },
        {
          img: "https://picsum.photos/id/234/600/350",
          title: "Solution for clean look working space",
          date: "20 jan 2020",
        },
        {
          img: "https://picsum.photos/id/233/600/350",
          title: "How to create a living room to love",
          date: "20 jan 2020",
        },
      ],
      rasmSoni: 0,
      caruselCircle: 0,
    };
  },
  computed: {},
  methods: {
    next() {
      if (this.slides.length - 4 >= this.rasmSoni) {
        this.caruselCircle++;
        if (this.caruselCircle > 2) {
          this.rasmSoni++;
        }
      } else {
        this.rasmSoni = 0;
        this.caruselCircle = 0;
      }
    },
    prev() {
      console.log(this.rasmSoni);
      console.log(this.caruselCircle);
      if (this.rasmSoni > 0) {
        if (this.caruselCircle <= 2) {
          this.rasmSoni--;
        }
      } else if (this.rasmSoni <= 0) {
        this.rasmSoni = this.slides.length - 3;
      }
      if (this.caruselCircle <= 0) {
        this.caruselCircle = this.slides.length - 1;
      } else if (this.caruselCircle <= this.slides.length) {
        this.caruselCircle--;
      }
    },
  },
  components: {
    Carousel,
    CarouselSlide,
  },
};
</script>

<style>
.btnSlideN {
  z-index: 20;
  right: 1%;
}
.btnSlideP {
  z-index: 10;
  left: 1%;
}
</style>
