<template>
  <label class="relative block">
    <span class="sr-only">Search</span>
    <span class="absolute inset-y-0 left-0 flex items-center pl-2">
      <svg class="h-5 w-5 fill-slate-300" viewBox="0 0 20 20"><!-- ... --></svg>
    </span>
    <input
      class="placeholder:italic placeholder:text-slate-400 block bg-white w-[200%] py-2 pl-9 pr-3 shadow-sm focus:outline-none focus:border-sky-500 focus:ring-sky-500 focus:ring-1 sm:text-sm"
      placeholder="Search for anything..."
      type="text"
      name="search"
    />
  </label>
</template>

<script>
export default {
  name: "Search",
};
</script>

<style></style>
