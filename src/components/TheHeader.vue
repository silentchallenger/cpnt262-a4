<script setup>
import TheNav from "./TheNav.vue";

defineProps({
  pageHeader: {
    type: String,
    default: "Base Page Header",
  },
});
</script>

<template>
  <header class="flex flex-col">
    <section class="flex items-center justify-between gap-4 bg-stone-800 p-4">
      <p class="text-2xl font-bold text-white">{{ pageHeader }}</p>
      <TheNav />
    </section>
    <slot></slot>
  </header>
</template>
