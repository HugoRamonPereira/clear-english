<template>
  <NuxtLayout name="auth">
    <div
      class="flex flex-col items-center justify-center mx-auto w-[500px] max-h-[600px] select-none"
    >
      <NuxtLink
        to="/"
        class="flex items-center gap-1 justify-center border border-gray-400 rounded-md px-4 h-10 text-gray-500 hover:border-gray-500 hover:bg-gray-100/90 hover:trasnsition-colors hover:duration-200 absolute top-6 left-6 dark:hover:bg-gray-900/50 dark:border-gray-500/50 dark:text-gray-500 focus-visible:outline-2 focus-visible:outline-violet-violetMain"
      >
        <ArrowLeft :size="18" :stroke-width="1.5" />
      </NuxtLink>
      <NuxtImg src="/nuxt-clear-english-signup-illustration.png" />
    </div>
    <template #form>
      <div
        class="flex flex-col items-center justify-center gap-4 w-full xl:w-[90%] select-none"
      >
        <div
          class="flex flex-col items-center justify-center gap-4 w-[90%] border border-gray-300 dark:border-gray-500/50 rounded-lg py-14"
        >
          <div class="text-2xl lg:text-3xl">
            <h1 class="dark:text-gray-300">Create Your Account</h1>
          </div>
          <div class="w-4/5 lg:w-3/4">
            <form class="flex flex-col gap-4">
              <FormField name="email">
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
              <FormField name="Password">
                <FormItem>
                  <FormLabel class="dark:text-gray-300">Password</FormLabel>
                  <FormControl>
                    <div class="relative w-full items-center">
                      <Input
                        v-model="password"
                        placeholder="Enter your password"
                        :type="inputPassType"
                        class="px-10 text-base dark:text-gray-300 border-[1.5px] border-gray-300 dark:border-gray-500 focus-visible:ring-transparent focus-visible:transition-colors focus-visible:duration-500 focus-visible:border-[1.5px] focus-visible:border-violet-violetMain dark:focus-visible:border-violet-violetMain"
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
                        class="absolute end-1 inset-y-0 flex items-center justify-center px-2 focus-visible:outline-2 focus-visible:outline-violet-violetMain"
                        @click.prevent="togglePassVisibility"
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
              <FormField name="Confirm Password">
                <FormItem>
                  <FormLabel class="dark:text-gray-300"
                    >Confirm Password</FormLabel
                  >
                  <FormControl>
                    <div class="relative w-full items-center">
                      <Input
                        v-model="confirmPassword"
                        placeholder="Confirm your password"
                        :type="inputConfirmPassType"
                        class="px-10 text-base dark:text-gray-300 border-[1.5px] border-gray-300 dark:border-gray-500 focus-visible:ring-transparent focus-visible:transition-colors focus-visible:duration-500 focus-visible:border-[1.5px] focus-visible:border-violet-violetMain dark:focus-visible:border-violet-violetMain"
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
                        class="absolute end-1 inset-y-0 flex items-center justify-center px-2 focus-visible:outline-2 focus-visible:outline-violet-violetMain"
                        @click.prevent="toggleConfirmPassVisibility"
                      >
                        <Eye
                          v-if="showConfirmPassword === true"
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
                <p class="text-gray-500">Already have an account?</p>
                <NuxtLink
                  to="/signin"
                  class="text-gray-500 underline decoration-gray-500 hover:text-gray-700 hover:decoration-gray-700 underline-offset-4 dark:hover:text-gray-400 dark:hover:decoration-gray-400 focus-visible:outline-2 focus-visible:outline-violet-violetMain"
                >
                  Sign in</NuxtLink
                >
              </div>
              <div class="flex items-center justify-center space-x-2 my-2">
                <div class="flex items-center gap-2 flex-row">
                  <Checkbox id="terms" class="border-gray-500" />
                  <label
                    for="terms"
                    class="peer-disabled:cursor-not-allowed peer-disabled:opacity-70 !-mr-1 text-gray-500"
                  >
                    I accept the
                  </label>
                </div>
                <NuxtLink
                  to="/terms"
                  target="_blank"
                  class="text-gray-500 underline decoration-gray-500 hover:text-gray-700 dark:hover:text-gray-400 hover:decoration-gray-700 underline-offset-4 dark:hover:decoration-gray-400 focus-visible:outline-2 focus-visible:outline-violet-violetMain"
                >
                  terms & conditions
                </NuxtLink>
              </div>
              <Button
                class="bg-violet-violetMain hover:bg-violet-violetMainHover transition-colors duration-300 text-base uppercase h-11"
                >Sign up</Button
              >
            </form>
          </div>
        </div>
        <div class="mt-10">
          <NuxtLink
            to="/"
            class="flex items-center gap-1 justify-center border border-gray-400 rounded-md px-4 h-10 text-gray-500 hover:border-gray-500 hover:bg-gray-100/90 hover:trasnsition-colors hover:duration-200 dark:hover:bg-gray-900/50 dark:border-gray-500/50 dark:text-gray-500 focus-visible:outline-2 focus-visible:outline-violet-violetMain"
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
import { Checkbox } from "@/components/ui/checkbox";

import { Mail, Lock, Eye, EyeOff, Home, ArrowLeft } from "lucide-vue-next";

useHead({
  title: "Sign Up",
});

definePageMeta({
  layout: false,
});

const password = ref("");
const confirmPassword = ref("");
const showPassword = ref(false);
const showConfirmPassword = ref(false);

const togglePassVisibility = () => {
  showPassword.value = !showPassword.value;
};

const toggleConfirmPassVisibility = () => {
  showConfirmPassword.value = !showConfirmPassword.value;
};

const inputPassType = computed(() => {
  return showPassword.value ? "text" : "password";
});

const inputConfirmPassType = computed(() => {
  return showConfirmPassword.value ? "text" : "password";
});
</script>
