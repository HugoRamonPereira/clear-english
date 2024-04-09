<template>
  <div class="flex">
    <div
      class="hidden w-1/2 h-screen sm:flex items-center justify-center border-r border-gray-300 dark:border-gray-500/50"
    >
      <div class="w-3/5">
        <NuxtImg src="/not-found.png" alt="Page not found" />
      </div>
    </div>
    <div
      class="w-full h-screen sm:w-1/2 flex flex-col items-center justify-center gap-6"
    >
      <div class="w-2/3 sm:hidden flex items-center justify-center mb-2">
        <NuxtImg src="/not-found.png" alt="Page not found" />
      </div>
      <p class="text-5xl text-gray-600 dark:text-gray-300">
        Error {{ error.statusCode }}
      </p>
      <p class="text-2xl text-gray-500 dark:text-gray-300">
        {{ error.message }}
      </p>
      <div class="w-3/4 text-center sm:w-full">
        <p class="text-gray-500 dark:text-gray-300">
          The URL you entered is invalid. Please enter a valid URL address.
        </p>
      </div>
      <TheLink
        to="/"
        class-name="flex items-center gap-2 justify-center border border-gray-300 rounded-md px-4 h-10 text-gray-400 hover:text-gray-500 hover:border-gray-400 hover:bg-gray-100/50 hover:trasnsition-colors hover:duration-200 dark:hover:bg-gray-900/50 dark:border-gray-500/50 dark:text-gray-500 mt-10"
      >
        Back to Home
        <Home :size="18" :stroke-width="1.5" />
      </TheLink>
    </div>
  </div>
</template>

<script setup>
import { Home } from "lucide-vue-next";

defineProps(["error"]);
</script>
