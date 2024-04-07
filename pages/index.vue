<template>
  <TheHeader />
  <TheHero />
  <TheHero />
  <TheFooter />
</template>

<script lang="ts" setup>
import TheHeader from "~/components/TheHeader.vue";
import TheFooter from "~/components/TheFooter.vue";
import TheHero from "~/components/TheHero.vue";

useHead({
  title: "Home",
});
</script>
