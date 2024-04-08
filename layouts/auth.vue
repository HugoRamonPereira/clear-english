<template>
  <div class="flex">
    <div
      class="w-1/2 h-screen flex items-center justify-center border-r border-b-gray-600"
    >
      <div class="w-4/5 h-5/6 flex items-center justify-center">
        <slot />
      </div>
    </div>
    <div class="w-1/2 flex items-center justify-center">
      <div class="w-4/5 h-4/6 flex items-center justify-center">
        <slot name="form" />
      </div>
    </div>
  </div>
</template>
