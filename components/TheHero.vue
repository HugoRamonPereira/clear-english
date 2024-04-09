<template>
  <section
    class="flex flex-col-reverse sm:flex-row h-full min-h-[400px] sm:min-h-[600px] w-full max-w-[1200px] mx-auto select-none"
  >
    <div
      class="w-5/6 sm:w-1/2 lg:w-3/5 flex flex-col gap-1.5 sm:gap-4 md:gap-2 items-center justify-center text-center mx-auto"
    >
      <h1 class="text-4xl sm:text-4xl lg:text-6xl font-bold">
        Conquer the world
      </h1>
      <h1 class="text-4xl sm:text-4xl lg:text-6xl font-bold">
        studying English
      </h1>
      <h1 class="text-4xl sm:text-4xl lg:text-6xl font-bold">with us</h1>
      <div class="w-4/5 sm:w-3/5 lg:w-full my-4">
        <h3
          class="flex items-center justify-center text-lg sm:text-2xl font-normal my-4 dark:text-gray-300"
        >
          Explore the many opportunites that await you
        </h3>
      </div>
      <Button
        class="text-base sm:text-xl font-normal flex gap-1 h-10 sm:h-12 bg-violet-violetMain text-white px-5 rounded-lg hover:bg-violet-violetMainHover"
      >
        <NuxtLink to="/signup" class="flex items-center gap-2" tabindex="-1">
          <p class="uppercase">Join us right now</p>
          <ArrowRight class="sm:hidden" :size="18" :stroke-width="1.8" />
          <ArrowRight class="hidden sm:block" :size="22" :stroke-width="1.8" />
        </NuxtLink>
      </Button>
    </div>
    <div
      class="w-3/5 sm:w-1/2 lg:w-2/5 flex items-center justify-center mx-auto md:mr-10 my-6 sm:mb-0"
    >
      <NuxtImg src="/nuxt-clear-english-illustration.png" />
    </div>
  </section>
</template>

<script lang="ts" setup>
import Button from "./ui/button/Button.vue";
import { ArrowRight } from "lucide-vue-next";
</script>
