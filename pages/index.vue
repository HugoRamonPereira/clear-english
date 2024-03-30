<template>
  <div class='border-b border-b-stone-300'>
    <header class='w-full max-w-[1200px] flex items-center justify-center mx-auto'>
      <TheHeader />
    </header>
  </div>
</template>

<script lang="ts" setup>
import TheHeader from '~/components/TheHeader.vue';

useHead({
  title: 'Home'
})
</script>
