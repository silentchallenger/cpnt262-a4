<script setup>
import AppButton from "./AppButton.vue";

defineProps({
  cardTitle: {
    type: String,
    default: "Default Card Title",
  },
  cardSubTitle: {
    type: String,
    default: "Default Card Sub Title",
  },
  cardText: {
    type: String,
    default: "Default Card Text",
  },
  cardUrl: String,
});
</script>

<template>
  <section class="m-4 max-w-xs rounded-md bg-slate-200 p-4">
    <img
      :src="cardUrl"
      :alt="cardTitle"
    />
    <h2 class="pt-4 text-xl font-bold">Travel to {{ cardTitle }}</h2>
    <h3 class="font-semibold">Starting from {{ cardSubTitle }}</h3>
    <p>
      Learn the history of {{ cardText }} with our guides that are best in
      industry. Eat the local dishes from local shops.
    </p>
    <section class="flex justify-end gap-4 pt-6">
      <AppButton
        bgColor="bg-white"
        txtColor="text-red-500"
        text="View"
      />
      <AppButton
        bgColor="bg-red-500"
        txtColor="text-white"
        text="Join"
      />
    </section>
  </section>
</template>
