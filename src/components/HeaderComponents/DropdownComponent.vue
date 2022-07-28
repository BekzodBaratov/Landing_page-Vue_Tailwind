<template>
  <div
    @click="setActive"
    class="relative focus:outline-none inline-block text-left font-medium text-gray-500 hover:text-gray-900"
  >
    <div>
      <button
        type="button"
        class="inline-flex text justify-center w-full rounded-md border-none px-4 py-2 bg-transparent font-medium text-gray-500 hover:text-gray-900 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-offset-gray-100 focus:ring-indigo-500"
        id="menu-button"
        aria-expanded="true"
        aria-haspopup="true"
      >
        {{ title }}
        <svg
          class="-mr-1 ml-2 h-5 w-5"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 20 20"
          fill="currentColor"
          aria-hidden="true"
        >
          <path
            fill-rule="evenodd"
            d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
            clip-rule="evenodd"
          />
        </svg>
      </button>
    </div>

    <div
      class="origin-top-right absolute right-0 mt-2 w-56 rounded-md shadow-lg bg-white ring-1 ring-black ring-opacity-5 focus:outline-none"
      role="menu"
      aria-orientation="vertical"
      aria-labelledby="menu-button"
      tabindex="-1"
      v-if="active"
    >
      <div class="py-1" role="none">
        <a
          v-for="product in products"
          :key="product"
          href="#"
          class="text-gray-700 hover:bg-gray-200 block px-4 py-2 text-sm"
          role="menuitem"
          tabindex="-1"
          id="menu-item-0"
          >{{ product }}</a
        >
      </div>
    </div>
  </div>
</template>

<script scoped>
export default {
  props: ["products", "title"],
  name: "DropdownComp",
  data() {
    return {
      active: false,
    };
  },
  methods: {
    setActive() {
      this.active = !this.active;
    },
  },
};
</script>

<style></style>
