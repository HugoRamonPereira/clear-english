<script setup lang="ts">
import {
  NavigationMenu,
  NavigationMenuContent,
  NavigationMenuItem,
  NavigationMenuLink,
  NavigationMenuList,
  NavigationMenuTrigger,
} from '@/components/ui/navigation-menu'
import { Button } from '@/components/ui/button'
import { LogIn, UserPlus } from 'lucide-vue-next';

</script>

<template>
  <div class='w-full flex items-center justify-between h-16'>
    <p class='font-normal'>Clear English</p>
    <NavigationMenu>
      <NavigationMenuList>
        <NavigationMenuItem>
          <NavigationMenuTrigger>Item One</NavigationMenuTrigger>
          <NavigationMenuContent>
            <NavigationMenuLink>Link</NavigationMenuLink>
          </NavigationMenuContent>
        </NavigationMenuItem>
      </NavigationMenuList>
    </NavigationMenu>
    <div class='font-light flex gap-4'>
      <Button
        class='flex gap-1 bg-white border border-violet-500 text-violet-500 py-1 px-4 rounded-lg hover:bg-violet-500 hover:text-white'>
        Sign in
        <LogIn :size="18" :stroke-width="1.5" />
      </Button>
      <Button
        class='flex gap-1 bg-white text-black border border-black py-1 px-4 rounded-lg hover:bg-black hover:text-white'>
        Sign up
        <UserPlus :size="18" :stroke-width="1.5" />
      </Button>
    </div>
  </div>
</template>
