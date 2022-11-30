<script setup>
defineProps({
  title: {
    type: String,
    default: "Default Title",
  },
  context: {
    type: String,
    default: "Default Content",
  },
  color: {
    type: String,
    default: "text-indigo-500",
  },
});
</script>

<template>
  <header class="p-2 text-center">
    <h1
      class="py-4 text-3xl lg:text-5xl"
      :class="color"
    >
      {{ title }}
    </h1>
    <p class="text-xl">{{ context }}</p>
    <slot></slot>
  </header>
</template>
