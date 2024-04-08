<template>
  <NuxtLayout name="auth">
    <div
      class="flex flex-col items-center justify-center mx-auto w-[400px] max-h-[500px]"
    >
      <NuxtLink
        to="/"
        class="flex items-center gap-1 justify-center border border-gray-300 dark:hover:bg-gray-900/50 dark:border-gray-500/50 rounded-md px-4 h-10 text-gray-400 hover:border-gray-400 hover:bg-gray-100/90 hover:trasnsition-colors hover:duration-200 absolute top-6 left-6"
      >
        <ArrowLeft :size="18" :stroke-width="1.5" />
      </NuxtLink>
      <NuxtImg src="/nuxt-clear-english-signin-illustration.png" />
    </div>
    <template #form>
      <div
        class="flex flex-col items-center justify-center gap-4 w-full xl:w-[90%]"
      >
        <div
          class="flex flex-col items-center justify-center gap-4 w-[90%] border border-gray-300 dark:border-gray-500/50 rounded-lg py-14"
        >
          <div class="text-2xl lg:text-3xl">
            <h1 class="dark:text-gray-300">Enter Your Credentials</h1>
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
                        class="pl-10 text-base dark:text-gray-300 border-gray-300 dark:border-gray-500 focus-visible:ring-0 focus-visible:transition-colors focus-visible:duration-500 focus-visible:border-[1.5px] focus-visible:border-violet-violetMain dark:focus-visible:border-violet-violetMain"
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
              <FormField name="Password">
                <FormItem>
                  <FormLabel class="dark:text-gray-300">Password</FormLabel>
                  <FormControl>
                    <div class="relative w-full items-center">
                      <Input
                        v-model="password"
                        placeholder="Enter your password"
                        :type="inputType"
                        class="px-10 text-base dark:text-gray-300 border-gray-300 dark:border-gray-500 focus-visible:ring-0 focus-visible:transition-colors focus-visible:duration-500 focus-visible:border-[1.5px] focus-visible:border-violet-violetMain dark:focus-visible:border-violet-violetMain"
                      />
                      <span
                        class="absolute start-1 inset-y-0 flex items-center justify-center px-2"
                      >
                        <Lock
                          class="size-5 text-muted-foreground stroke-gray-400/75"
                          :stroke-width="1.5"
                        />
                      </span>
                      <button
                        class="absolute end-1 inset-y-0 flex items-center justify-center px-2"
                        @click.prevent="toggleVisibility"
                      >
                        <Eye
                          v-if="showPassword === true"
                          class="size-5 text-muted-foreground stroke-gray-400/75"
                          :stroke-width="1.5"
                        />
                        <EyeOff
                          v-else
                          class="size-5 text-muted-foreground stroke-gray-400/75"
                          :stroke-width="1.5"
                        />
                      </button>
                    </div>
                  </FormControl>
                  <FormDescription />
                  <FormMessage />
                </FormItem>
              </FormField>
              <div
                class="flex flex-col xl:flex-row items-center justify-center gap-2"
              >
                <p class="text-gray-500">Don't have an account yet?</p>
                <NuxtLink
                  to="/signup"
                  class="text-gray-500 underline decoration-gray-500 hover:text-gray-700 hover:decoration-gray-700 underline-offset-4 dark:hover:text-gray-400 dark:hover:decoration-gray-400"
                >
                  Create account</NuxtLink
                >
              </div>
              <div class="flex items-center justify-center mb-2">
                <NuxtLink
                  to="/forgot-password"
                  class="text-gray-500 underline decoration-gray-500 hover:text-gray-700 hover:decoration-gray-700 underline-offset-4 dark:hover:text-gray-400 dark:hover:decoration-gray-400"
                >
                  Forgot your password?</NuxtLink
                >
              </div>
              <Button
                class="dark:text-gray-300 dark:hover:text-gray-400 bg-violet-violetMain hover:bg-violet-violetMainHover transition-colors duration-300 text-base uppercase h-11 dark:hover:decoration-gray-400"
                >Sign in</Button
              >
            </form>
          </div>
        </div>
        <div class="mt-10">
          <NuxtLink
            to="/"
            class="flex items-center gap-2 justify-center border border-gray-300 rounded-md px-4 h-10 text-gray-400 hover:text-gray-500 hover:border-gray-400 hover:bg-gray-100/50 hover:trasnsition-colors hover:duration-200 dark:hover:bg-gray-900/50 dark:border-gray-500/50 dark:text-gray-500"
          >
            Back to Home
            <Home :size="18" :stroke-width="1.5" />
          </NuxtLink>
        </div>
      </div>
    </template>
  </NuxtLayout>
</template>

<script lang="ts" setup>
import { ref, computed } from "vue";
import {
  FormControl,
  FormDescription,
  FormField,
  FormItem,
  FormLabel,
  FormMessage,
} from "@/components/ui/form";

import { Mail, Lock, Eye, EyeOff, Home, ArrowLeft } from "lucide-vue-next";

useHead({
  title: "Sign In",
});

definePageMeta({
  layout: false,
});

const password = ref("");
const showPassword = ref(false);

const toggleVisibility = () => {
  showPassword.value = !showPassword.value;
};

const inputType = computed(() => {
  return showPassword.value ? "text" : "password";
});
</script>
