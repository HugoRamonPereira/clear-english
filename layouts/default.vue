<template>
  <TheHeader />
  <div class="flex flex-col-reverse w-full max-w-[1200px] m-auto select-none">
    <slot />
  </div>
  <TheFooter />
</template>

<script lang="ts" setup>
import TheHeader from "~/components/TheHeader.vue";
import TheFooter from "~/components/TheFooter.vue";
</script>
