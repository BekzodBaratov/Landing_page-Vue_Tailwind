<template>
  <slot></slot>
  <div class="absolute bottom-2 left-1/2 -translate-x-1/2 kallaUxshamadi flex gap-4">
    <span
      class="w-3 h-3 rounded-full bg-orange-600"
      v-for="(n, key) in controlCircle"
      :class="key == caruselCircle ? 'outline outline-offset-4 outline-1 outline-orange-600' : ''"
      :key="key"
    ></span>
  </div>
</template>

<script>
export default {
  methods: {},
  props: ["controlCircle", "caruselCircle"],
};
</script>

<style>
.kallaUxshamadi {
  z-index: 30;
}
</style>
