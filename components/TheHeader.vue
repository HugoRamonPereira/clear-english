<template>
  <header class='max-w-full border-b border-b-stone-300 px-4 sm:px-0'>
    <div class='sm:max-w-[1200px] flex items-center justify-center mx-auto'>
      <div class='w-full flex items-center justify-between h-16'>
        <div class='flex items-center gap-14'>
          <NuxtLink to='/'>
            <p class='font-normal'>Clear English</p>
          </NuxtLink>
          <NavigationMenu class='hidden sm:flex'>
            <NavigationMenuList>
              <NavigationMenuItem>
                <NavigationMenuTrigger>Getting started</NavigationMenuTrigger>
                <NavigationMenuContent>
                  <ul class="grid gap-3 p-6 md:w-[400px] lg:w-[500px] lg:grid-cols-[minmax(0,.75fr)_minmax(0,1fr)]">
                    <li class="row-span-3">
                      <NavigationMenuLink as-child>
                        <a class="flex h-full w-full select-none flex-col justify-end rounded-md bg-gradient-to-b from-muted/50 to-muted p-6 no-underline outline-none focus:shadow-md"
                          href="/">
                          <img src="https://www.radix-vue.com/logo.svg" class="h-6 w-6">
                          <div class="mb-2 mt-4 text-lg font-medium">
                            shadcn/ui
                          </div>
                          <p class="text-sm leading-tight text-muted-foreground">
                            Beautifully designed components built with Radix UI and
                            Tailwind CSS.
                          </p>
                        </a>
                      </NavigationMenuLink>
                    </li>
                    <li href="/docs" title="Introduction">
                      Re-usable components built using Radix UI and Tailwind CSS.
                    </li>
                    <li href="/docs/installation" title="Installation">
                      How to install dependencies and structure your app.
                    </li>
                    <li href="/docs/primitives/typography" title="Typography">
                      Styles for headings, paragraphs, lists...etc
                    </li>
                  </ul>
                </NavigationMenuContent>
              </NavigationMenuItem>
              <NavigationMenuItem>
                <NavigationMenuTrigger>Components</NavigationMenuTrigger>
                <NavigationMenuContent>
                  <ul class="grid w-[400px] gap-3 p-4 md:w-[500px] md:grid-cols-2 lg:w-[600px] ">
                    <li v-for="component in components" :key="component.title" :title="component.title"
                      :href="component.href">
                      {{ component.description }}
                    </li>
                  </ul>
                </NavigationMenuContent>
              </NavigationMenuItem>
              <NavigationMenuItem>
                <NavigationMenuLink href="/docs" :class="navigationMenuTriggerStyle()">
                  <NuxtLink to='/membership' class='flex gap-1'>
                    Go Premium
                    <Crown :size="18" :stroke-width="1.5" />
                  </NuxtLink>
                </NavigationMenuLink>
              </NavigationMenuItem>
            </NavigationMenuList>
          </NavigationMenu>
        </div>

        <div class='flex items-center justify-center gap-4'>
          <div>
            <TheSearch />
          </div>
          <div class='hidden sm:flex'>
            <ThemeSwitcher />
          </div>
          <div class='hidden sm:flex font-light gap-4'>
            <Button class='flex gap-1 bg-violet-500 text-white py-1 px-4 rounded-lg hover:bg-violet-600'>
              <NuxtLink to='signin'>
                Sign in
              </NuxtLink>
              <LogIn :size="18" :stroke-width="1.5" />
            </Button>
            <Button
              class='flex gap-1 bg-white text-black border border-black py-1 px-4 rounded-lg hover:bg-slate-800 hover:text-white'>
              <NuxtLink to='signup'>
                Sign up
              </NuxtLink>
              <UserPlus :size="18" :stroke-width="1.5" />
            </Button>
          </div>
          <div>
            <Button variant='outline' class='sm:hidden px-2'>
              <Menu :size="20" :stroke-width="1.5" />
            </Button>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script setup lang="ts">

import {
  NavigationMenu,
  NavigationMenuContent,
  NavigationMenuItem,
  NavigationMenuLink,
  NavigationMenuList,
  NavigationMenuTrigger,
  navigationMenuTriggerStyle,
} from '@/components/ui/navigation-menu'
import { Button } from '@/components/ui/button'
import { LogIn, UserPlus, Crown, Menu } from 'lucide-vue-next';

const components: { title: string, href: string, description: string }[] = [
  {
    title: 'Alert Dialog',
    href: '/docs/primitives/alert-dialog',
    description:
      'A modal dialog that interrupts the user with important content and expects a response.',
  },
  {
    title: 'Hover Card',
    href: '/docs/primitives/hover-card',
    description:
      'For sighted users to preview content available behind a link.',
  },
  {
    title: 'Progress',
    href: '/docs/primitives/progress',
    description:
      'Displays an indicator showing the completion progress of a task, typically displayed as a progress bar.',
  },
  {
    title: 'Scroll-area',
    href: '/docs/primitives/scroll-area',
    description: 'Visually or semantically separates content.',
  },
  {
    title: 'Tabs',
    href: '/docs/primitives/tabs',
    description:
      'A set of layered sections of content—known as tab panels—that are displayed one at a time.',
  },
  {
    title: 'Tooltip',
    href: '/docs/primitives/tooltip',
    description:
      'A popup that displays information related to an element when the element receives keyboard focus or the mouse hovers over it.',
  },
]

</script>
