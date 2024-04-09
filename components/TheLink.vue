<template>
  <NuxtLink :to="to" :class="className">
    <slot />
  </NuxtLink>
</template>

<script setup>
defineProps({
  to: {
    type: [String, Object],
    required: true,
  },
  className: {
    type: String,
    default: "",
  },
});
</script>
