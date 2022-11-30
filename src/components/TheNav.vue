<script setup></script>

<template>
  <nav>
    <ul class="flex gap-4">
      <li>
        <RouterLink
          to="/"
          class="p-4 text-xl font-bold text-slate-100 hover:bg-slate-100 hover:text-black"
          >Home</RouterLink
        >
      </li>
      <li>
        <RouterLink
          to="/about"
          class="p-4 text-xl font-bold text-slate-100 hover:bg-slate-100 hover:text-black"
          >About</RouterLink
        >
      </li>
      <slot></slot>
    </ul>
  </nav>
</template>
