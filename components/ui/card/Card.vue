<script setup lang="ts">
import type { HTMLAttributes } from "vue";
import { cn } from "@/lib/utils";

const props = defineProps<{
  class?: HTMLAttributes["class"];
}>();
</script>

<template>
  <div
    :class="
      cn(
        'rounded-lg border bg-card text-card-foreground shadow-sm hover:border-violet-600 hover:-translate-y-2 hover:transition-transform hover:duration-300 cursor-pointer transition-colors duration-500',
        props.class,
      )
    "
  >
    <slot />
  </div>
</template>
