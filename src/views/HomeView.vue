<script setup>
import AppMain from "../components/AppMain.vue";
import AppCard from "../components/AppCard.vue";
import AppHeader from "../components/AppHeader.vue";
import AppList from "../components/AppList.vue";
import AppListItem from "../components/AppListItem.vue";
import TheHero from "../components/TheHero.vue";

const cardInfo = [
  {
    url: "/egypt.jpg",
    title: "Egypt",
    subtitle: "$600",
    text: "Egypt",
  },
  {
    url: "/japan.jpg",
    title: "Japan",
    subtitle: "$600",
    text: "Japan",
  },
  {
    url: "/china.jpg",
    title: "China",
    subtitle: "$600",
    text: "China",
  },
  {
    url: "/paris.jpg",
    title: "France",
    subtitle: "$600",
    text: "France",
  },
];

const advInfo = [
  {
    title: "Eget pellentesque odio urna.",
    text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Purus sit nisl turpis condimentum malesuada pulvinar varius velit. Urna, vestibulum, ullamcorper lorem ac eu. Consectetur nisl, sed in convallis in mattis urna.",
  },
  {
    title: "Eget pellentesque odio urna.",
    text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Purus sit nisl turpis condimentum malesuada pulvinar varius velit. Urna, vestibulum, ullamcorper lorem ac eu. Consectetur nisl, sed in convallis in mattis urna.",
  },
  {
    title: "Eget pellentesque odio urna.",
    text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Purus sit nisl turpis condimentum malesuada pulvinar varius velit. Urna, vestibulum, ullamcorper lorem ac eu. Consectetur nisl, sed in convallis in mattis urna.",
  },
  {
    title: "Eget pellentesque odio urna.",
    text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Purus sit nisl turpis condimentum malesuada pulvinar varius velit. Urna, vestibulum, ullamcorper lorem ac eu. Consectetur nisl, sed in convallis in mattis urna.",
  },
];
</script>

<template>
  <TheHero />
  <AppMain>
    <AppHeader
      title="Our Best Deals"
      context="You can see the our best seasonal deals to travel different countries that you can enjoy."
      color="text-blue-500"
    />
    <section class="flex flex-wrap justify-center">
      <AppCard
        v-for="card in cardInfo"
        :key="card.id"
        :cardUrl="card.url"
        :cardTitle="card.title"
        :cardSubTitle="card.subtitle"
        :cardText="card.text"
      >
      </AppCard>
    </section>
    <AppHeader
      title="Our Advantages"
      context="We have many different advantages that puts us in a different category compared to other firms."
      color="text-blue-500"
    />
    <section
      class="m-6 flex max-w-5xl flex-col items-center justify-center gap-4 md:flex-row lg:mx-auto"
    >
      <AppList>
        <AppListItem class="flex flex-col flex-wrap">
          <li
            v-for="info in advInfo"
            :key="info.id"
          >
            <h2 class="text-lg font-bold">{{ info.title }}</h2>
            <p>{{ info.text }}</p>
          </li>
        </AppListItem>
      </AppList>
      <img
        class="w-80"
        src="/scenery.jpg"
        alt="Scenery Image"
      />
    </section>
  </AppMain>
</template>
