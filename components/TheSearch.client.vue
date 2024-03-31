<template>
  <Dialog>
    <DialogTrigger>
      <Button variant='outline' class='w-[120px] sm:w-[220px] flex justify-between' @click='handleOpenChange'>
        <p class='hidden sm:block'>Search website...</p>
        <p class='sm:hidden'>Search...</p>
        <Search class='sm:hidden' :size="18" :stroke-width="1.5" />
        <div class='hidden sm:flex items-center gap-0.5 text-xs border border-1 p-1 px-1.5 -mr-2 rounded-md bg-gray-50'>
          <Command :size="11" :stroke-width="2" />
          K
        </div>
      </Button>
    </DialogTrigger>
  </Dialog>
  <CommandDialog v-model:open="open">
    <CommandInput placeholder="Type a command or search..." class='pr-8' />
    <CommandList>
      <CommandEmpty>No results found.</CommandEmpty>
      <CommandGroup heading="Suggestions">
        <CommandItem value="courses" class='flex items-center gap-1.5'>
          <NotebookPen :size="18" :stroke-width="1.5" />
          Courses
        </CommandItem>
        <CommandItem value="exercises" class='flex items-center gap-1.5'>
          <BookOpenText :size="18" :stroke-width="1.5" />
          Exercises
        </CommandItem>
        <CommandItem value="listening" class='flex items-center gap-1.5'>
          <Headphones :size="18" :stroke-width="1.5" />
          Listening
        </CommandItem>
      </CommandGroup>
      <CommandSeparator />
      <CommandGroup heading="Settings">
        <CommandItem value="profile" class='flex items-center gap-1.5'>
          <User :size="18" :stroke-width="1.5" />
          Profile
        </CommandItem>
        <CommandItem value="billing" class='flex items-center gap-1.5'>
          <CircleDollarSign :size="18" :stroke-width="1.5" />
          Billing
        </CommandItem>
        <CommandItem value="settings" class='flex items-center gap-1.5'>
          <Settings :size="18" :stroke-width="1.5" />
          Settings
        </CommandItem>
      </CommandGroup>
    </CommandList>
  </CommandDialog>
</template>

<script setup lang="ts">
import { useMagicKeys } from '@vueuse/core'
import { Command, NotebookPen, BookOpenText, Headphones, User, CircleDollarSign, Settings } from 'lucide-vue-next'
import { ref, watch } from 'vue'
import {
  CommandDialog,
  CommandEmpty,
  CommandGroup,
  CommandInput,
  CommandItem,
  CommandList,
  CommandSeparator,
} from '@/components/ui/command'
import { Dialog, DialogTrigger } from '@/components/ui/dialog'
import { Search } from 'lucide-vue-next';

const open = ref(false)

const { Meta_K, Ctrl_K } = useMagicKeys({
  passive: false,
  onEventFired(e) {
    if (e.key === 'k' && (e.metaKey || e.ctrlKey))
      e.preventDefault()
  },
})

watch([Meta_K, Ctrl_K], (v) => {
  if (v[0] || v[1])
    handleOpenChange()
})

function handleOpenChange() {
  open.value = !open.value
}
</script>