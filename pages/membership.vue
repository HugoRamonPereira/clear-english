<template>
  <div class="flex flex-col sm:h-[calc(100vh-172px)] justify-center">
    <div class="flex flex-col gap-6 text-center py-10 px-10 sm:px-0">
      <p class="text-4xl font-bold text-gray-800">
        Do you want to become a member?
      </p>
      <p class="tracking-wide">
        Check our plans below and choose the one that best fits your needs
      </p>
    </div>
    <div
      class="flex flex-col sm:flex-row items-center justify-evenly gap-6 mt-4"
    >
      <ThePlanCard title="Basic" description="Restricted Access" :price="0" />
      <ThePlanCard
        title="Lifetime"
        description="Access to everything forever"
        :price="500"
      />
      <ThePlanCard
        title="Monthly"
        description="Access to everything for as long as you pay"
        :price="20"
      />
    </div>
    <div class="mt-14 w-fit mx-auto justify-center">
      <NuxtLink
        to="/"
        class="flex items-center gap-2 justify-center border border-gray-300 rounded-md px-4 h-10 text-gray-400 hover:text-gray-500 hover:border-gray-400 hover:bg-gray-100/50 hover:trasnsition-colors hover:duration-200 dark:hover:bg-gray-900/50 dark:border-gray-500/50 dark:text-gray-500 focus-visible:outline-2 focus-visible:outline-violet-violetMain"
      >
        Back to Home
        <Home :size="18" :stroke-width="1.5" />
      </NuxtLink>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { Home } from "lucide-vue-next";

useHead({
  title: "Membership",
});
</script>
