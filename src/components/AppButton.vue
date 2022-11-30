<script setup>
defineProps({
  text: {
    type: String,
    default: "Button",
  },
  bgColor: {
    type: String,
    default: "bg-red-300",
  },
  txtColor: {
    type: String,
    default: "text-white",
  },
});
</script>

<template>
  <button
    class="max-w-30 rounded-2xl font-reemkufi"
    :class="bgColor"
  >
    <a
      class="m-auto block px-8 py-3 text-center text-dynamicA no-underline hover:bg-darkblue hover:transition-all hover:ease-out active:bg-white active:text-red-500 active:shadow-none"
      :class="txtColor"
      href="/"
      target="_blank"
      >{{ text }}</a
    >
  </button>
</template>
