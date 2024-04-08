<template>
  <TheHero />
  <TheHero />
</template>

<script lang="ts" setup>
import TheHero from "~/components/TheHero.vue";

useHead({
  title: "Home",
});

definePageMeta({
  layout: "default",
});
</script>
