<template>
  <div class="flex">
    <div
      class="hidden w-1/2 h-screen sm:flex items-center justify-center border-r border-gray-300 dark:border-gray-500/50"
    >
      <div class="w-4/5 h-5/6 flex items-center justify-center">
        <NuxtLink
          to="/"
          class="flex items-center gap-1 justify-center border border-gray-300 dark:hover:bg-gray-900/50 dark:border-gray-500/50 rounded-md px-4 h-10 text-gray-400 hover:border-gray-400 hover:bg-gray-100/90 hover:trasnsition-colors hover:duration-200 absolute top-6 left-6 focus-visible:outline-2 focus-visible:outline-violet-violetMain"
        >
          <ArrowLeft :size="18" :stroke-width="1.5" />
        </NuxtLink>
        <slot />
      </div>
    </div>
    <div
      class="w-full h-screen sm:w-1/2 flex flex-col items-center justify-center"
    >
      <div class="w-full lg:w-4/5 h-4/6 flex items-center justify-center">
        <slot name="form" />
      </div>
      <div class="mt-10">
        <NuxtLink
          to="/"
          class="flex items-center gap-2 justify-center border border-gray-300 rounded-md px-4 h-10 text-gray-400 hover:text-gray-500 hover:border-gray-400 hover:bg-gray-100/50 hover:trasnsition-colors hover:duration-200 dark:hover:bg-gray-900/50 dark:border-gray-500/50 dark:text-gray-500 focus-visible:outline-2 focus-visible:outline-violet-violetMain"
        >
          Back to Home
          <Home :size="18" :stroke-width="1.5" />
        </NuxtLink>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ArrowLeft, Home } from "lucide-vue-next";
</script>
