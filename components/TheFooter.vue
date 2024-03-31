<template>
  <footer class='max-w-full border-t border-t-stone-300 px-4 mt-6'>
    <div class='max-w-[1200px] h-20 flex items-center justify-between mx-auto'>
      <div>Clear English</div>
      <div class='flex'>
        <ul class='flex gap-2 sm:gap-4'>
          <li>
            <NuxtLink to='https://hugoramonpereira.dev/' target='_blank'>
              <Globe :size="20" :stroke-width="1.5" />
            </NuxtLink>
          </li>
          <li>
            <NuxtLink to='https://www.linkedin.com/in/hugo-ramon-pereira/' target='_blank'>
              <Linkedin :size="20" :stroke-width="1.5" />
            </NuxtLink>
          </li>
          <li>
            <NuxtLink to='https://github.com/HugoRamonPereira' target='_blank'>
              <Github :size="20" :stroke-width="1.5" />
            </NuxtLink>
          </li>
          <li>
            <NuxtLink to='https://www.instagram.com/hramon_pereira' target='_blank'>
              <Instagram :size="20" :stroke-width="1.5" />
            </NuxtLink>
          </li>
        </ul>
      </div>
      <div>
        <p class='flex'>&copy;&nbsp;{{ year }}
        <p class='hidden sm:block'>&nbsp;- All Rights Reserved</p>
        </p>
      </div>
    </div>
  </footer>
</template>

<script lang="ts" setup>
const year = new Date().getFullYear()

import { Globe, Linkedin, Github, Instagram } from 'lucide-vue-next'; 
</script>

<style scoped></style>
