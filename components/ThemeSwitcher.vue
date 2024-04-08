<template>
  <Button
    variant="outline"
    class="w-[50px] border-gray-400 hover:border-gray-500 text-gray-500 hover:text-gray-600 dark:bg-transparent dark:text-gray-300 dark:border-gray-300/50 dark:hover:bg-gray-900"
    @click="setColorTheme($colorMode.preference === 'dark' ? 'light' : 'dark')"
  >
    <Sun
      v-if="$colorMode.preference === 'dark'"
      :size="18"
      :stroke-width="1.5"
      class="absolute h-[1.2rem] w-[1.2rem]"
    />
    <Moon
      v-if="$colorMode.preference === 'light'"
      :size="20"
      :stroke-width="1.5"
      class="h-[1.2rem] w-[1.2rem]"
    />
    <span class="sr-only">Toggle theme</span>
  </Button>
</template>

<script setup lang="ts">
import { Button } from "@/components/ui/button";
import { Sun, Moon } from "lucide-vue-next";

type Theme = "light" | "dark";

const setColorTheme = (newTheme: Theme) => {
  useColorMode().preference = newTheme;
};
</script>
