<template>
  <button
    class="carousel-control transition-all hover:-translate-x-1 left flex items-center justify-center"
    @click="$emit('prev')"
  >
    <p class="">
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
  <button
    class="carousel-control transition-all hover:translate-x-1 right flex items-center justify-center"
    @click="$emit('next')"
  >
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
  </button>
</template>

<script>
export default {
  emits: ["prev", "next"], // vue v3
};
</script>

<style scoped>
.carousel-control {
  background-color: #e89f71;
  border: none;
  position: absolute;
  height: 2.5rem;
  width: 2.5rem;
  border-radius: 50%;
  top: calc(50% - 25px);
  color: #f3f3f3;
  cursor: pointer;
}
.left {
  right: 3.5rem;
}
.right {
  right: 0.5rem;
}
</style>
