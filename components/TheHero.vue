<template>
  <section class='flex h-full min-h-[600px] w-full max-w-[1200px] mx-auto'>
    <div class='w-3/5 flex flex-col gap-4 items-center justify-center text-center'>
      <h1 class='text-6xl font-bold'>Conquer the world</h1>
      <h1 class='text-6xl font-bold'>studying English</h1>
      <h1 class='text-6xl font-bold'>with us</h1>
      <h3 class='text-2xl font-normal my-4'>Explore the many opportunites that await you</h3>
      <Button class='text-xl font-normal flex gap-1 h-12 bg-violet-500 text-white px-5 rounded-lg hover:bg-violet-600'>
        <NuxtLink to='/signup' class='flex items-center gap-2'>
          Join us right now
          <ArrowRight :size="22" :stroke-width="1.8" />
        </NuxtLink>
      </Button>
    </div>
    <div class='w-2/5 flex items-center justify-center'>
      <NuxtImg src='/nuxt-clear-english-illustration.png' />
    </div>
  </section>
</template>

<script lang="ts" setup>
import Button from './ui/button/Button.vue';
import { ArrowRight } from 'lucide-vue-next';
</script>
