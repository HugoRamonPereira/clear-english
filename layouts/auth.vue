<template>
  <div class="flex">
    <div
      class="hidden w-1/2 h-screen sm:flex items-center justify-center border-r border-gray-300 dark:border-gray-500/50"
    >
      <div class="w-4/5 h-5/6 flex items-center justify-center">
        <slot />
      </div>
    </div>
    <div
      class="w-full h-screen sm:w-1/2 flex flex-col items-center justify-center"
    >
      <div class="w-full lg:w-4/5 h-4/6 flex items-center justify-center">
        <slot name="form" />
      </div>
    </div>
  </div>
</template>
