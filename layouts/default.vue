<template>
  <TheHeader />
  <slot />
  <TheFooter />
</template>

<script lang="ts" setup>
import TheHeader from "~/components/TheHeader.vue";
import TheFooter from "~/components/TheFooter.vue";
</script>
