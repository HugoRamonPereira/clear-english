<template>
  <footer class='w-full border-t border-t-stone-300'>
    <div class=' w-[1200px] h-20 flex items-center justify-between mx-auto'>
      <div>Clear English</div>
      <div class='flex'>
        <p>Developed by - &nbsp;</p>
        <NuxtLink to='https://hugoramonpereira.dev/' target='_blank'>Hugo Ramon Pereira</NuxtLink>
      </div>
      <div>
        <p>&copy;&nbsp;{{ year }} - All Rights Reserved</p>
      </div>
    </div>
  </footer>
</template>

<script lang="ts" setup>
const year = new Date().getFullYear()
</script>

<style scoped></style>
