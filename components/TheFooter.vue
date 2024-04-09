<template>
  <footer
    class="max-w-full border-t border-t-stone-300 dark:border-t-gray-700 px-4 mt-6 select-none"
  >
    <div class="max-w-[1200px] h-20 flex items-center justify-between mx-auto">
      <div>Clear English</div>
      <div class="flex">
        <ul class="flex gap-2 sm:gap-4">
          <li
            class="text-gray-500 hover:text-black transition-colors duration-200 dark:text-gray-300 dark:hover:text-white dark:transition-colors dark:duration-200"
          >
            <NuxtLink
              to="https://hugoramonpereira.dev/"
              target="_blank"
              class="focus-visible:outline-2 focus-visible:outline-violet-violetMain"
            >
              <Globe :size="20" :stroke-width="1.5" />
            </NuxtLink>
          </li>
          <li
            class="text-gray-500 hover:text-black transition-colors duration-200 dark:text-gray-300 dark:hover:text-white dark:transition-colors dark:duration-200"
          >
            <NuxtLink
              to="https://www.linkedin.com/in/hugo-ramon-pereira/"
              target="_blank"
              class="focus-visible:outline-2 focus-visible:outline-violet-violetMain"
            >
              <Linkedin :size="20" :stroke-width="1.5" />
            </NuxtLink>
          </li>
          <li
            class="text-gray-500 hover:text-black transition-colors duration-200 dark:text-gray-300 dark:hover:text-white dark:transition-colors dark:duration-200"
          >
            <NuxtLink
              to="https://github.com/HugoRamonPereira"
              target="_blank"
              class="focus-visible:outline-2 focus-visible:outline-violet-violetMain"
            >
              <Github :size="20" :stroke-width="1.5" />
            </NuxtLink>
          </li>
          <li
            class="text-gray-500 hover:text-black transition-colors duration-200 dark:text-gray-300 dark:hover:text-white dark:transition-colors dark:duration-200"
          >
            <NuxtLink
              to="https://www.instagram.com/hramon_pereira"
              target="_blank"
              class="focus-visible:outline-2 focus-visible:outline-violet-violetMain"
            >
              <Instagram :size="20" :stroke-width="1.5" />
            </NuxtLink>
          </li>
        </ul>
      </div>
      <div>
        <span class="flex text-gray-500 dark:text-gray-300"
          >&copy;&nbsp;{{ year }}
          <span class="hidden sm:block">&nbsp;- All Rights Reserved</span>
        </span>
      </div>
    </div>
  </footer>
</template>

<script lang="ts" setup>
const year = new Date().getFullYear();

import { Globe, Linkedin, Github, Instagram } from "lucide-vue-next";
</script>

<style scoped></style>
