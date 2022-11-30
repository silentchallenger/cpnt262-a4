<script setup>
import AppButton from "./AppButton.vue";
</script>

<template>
  <section
    class="m-0 flex h-hero flex-col justify-between bg-hero-section bg-cover bg-center bg-no-repeat text-center bg-blend-darken"
  >
    <h1 class="mb-0 mt-8 font-reemkufi text-dynamicH font-bold text-softorange">
      Discover the World
    </h1>
    <p class="my-16 mx-auto max-w-30 text-dynamicP text-white 45em:m-auto">
      Experience world with your own eyes rather than through screen.
    </p>
    <section class="my-12 flex justify-center gap-8">
      <AppButton
        bgColor="bg-white"
        txtColor="text-red-500"
        text="View"
      />
      <AppButton
        bgColor="bg-red-500"
        txtColor="text-white"
        text="Book"
      />
    </section>
  </section>
</template>
