<template>
  <NuxtLayout name="auth">
    <div>
      <div
        class="flex flex-col items-center justify-center mx-auto w-[600px] max-h-[500px] select-none"
      >
        <NuxtImg src="/nuxt-clear-english-forgot-pass.png" />
      </div>
    </div>
    <template #form>
      <div
        class="flex flex-col items-center justify-center gap-4 w-[90%] border border-gray-300 dark:border-gray-500/50 rounded-lg py-14"
      >
        <div class="text-center flex flex-col gap-4">
          <p class="text-2xl lg:text-3xl dark:text-gray-300">
            Recover Your Password
          </p>
          <p class="text-base lg:text-lg">
            We will send you a link for you to create a new password
          </p>
        </div>
        <div class="w-4/5 lg:w-3/4">
          <form class="flex flex-col gap-4">
            <FormField name="Email">
              <FormItem>
                <FormLabel class="dark:text-gray-300">Email</FormLabel>
                <FormControl>
                  <div class="relative w-full items-center">
                    <Input
                      placeholder="Enter your email"
                      class="pl-10 text-base dark:text-gray-300 border-[1.5px] border-gray-300 dark:border-gray-500 focus-visible:ring-transparent focus-visible:transition-colors focus-visible:duration-500 focus-visible:border-[1.5px] focus-visible:border-violet-violetMain dark:focus-visible:border-violet-violetMain"
                    />
                    <span
                      class="absolute start-1 inset-y-0 flex items-center justify-center px-2"
                    >
                      <Mail
                        class="size-5 text-muted-foreground stroke-gray-400/75"
                        :stroke-width="1.5"
                      />
                    </span>
                  </div>
                </FormControl>
                <FormDescription />
                <FormMessage />
              </FormItem>
            </FormField>
            <Button
              class="dark:text-gray-300 dark:hover:text-gray-400 bg-violet-violetMain hover:bg-violet-violetMainHover transition-colors duration-300 text-base uppercase h-11 dark:hover:decoration-gray-400"
              >Send Email</Button
            >
          </form>
        </div>
      </div>
    </template>
  </NuxtLayout>
</template>

<script lang="ts" setup>
import { Mail } from "lucide-vue-next";

definePageMeta({
  layout: false,
});

useHead({
  title: "Forgot Password",
});
</script>
