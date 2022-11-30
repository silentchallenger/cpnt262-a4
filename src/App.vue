<script setup>
import { RouterLink, RouterView } from "vue-router";
import TheHeader from "./components/TheHeader.vue";
import TheFooter from "./components/TheFooter.vue";
</script>

<template>
  <div class="flex min-h-screen flex-col">
    <TheHeader page-header="Amy's Travel Agency" />

    <RouterView class="grow" />

    <TheFooter />
  </div>
</template>
