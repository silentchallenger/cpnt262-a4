<script setup>
import { ref } from "vue";
import AppMain from "../components/AppMain.vue";
import AppHeader from "../components/AppHeader.vue";
import AppList from "../components/AppList.vue";
import AppListItem from "../components/AppListItem.vue";
import AppButton from "../components/AppButton.vue";

const showList = ref(false);
const listToggle = () => (showList.value = !showList.value);

const winnerList = [
  {
    name: "Adam",
    lastName: "Smith",
  },
  {
    name: "George",
    lastName: "Russel",
  },
  {
    name: "Lewis",
    lastName: "Hamilton",
  },
];
</script>

<template>
  <AppMain>
    <AppHeader
      title="About Page"
      context="This page is still in design process."
    />
    <AppHeader
      title="Ticket Winners"
      context="These are the lucky people who won the grand prize."
    />
    <section class="p-4 text-center">
      <AppButton
        @click.prevent="listToggle"
        text="Show Winner List"
      />
      <AppList
        v-show="showList"
        class="p-4"
      >
        <AppListItem
          v-for="winner in winnerList"
          :key="winner.id"
        >
          <p class="p-2 text-lg">{{ winner.name }} {{ winner.lastName }}</p>
        </AppListItem>
      </AppList>
    </section>
  </AppMain>
</template>
