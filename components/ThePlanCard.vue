<template>
  <div>
    <Card class="w-[380px]">
      <CardHeader>
        <CardTitle class="text-center text-3xl">{{ title }}</CardTitle>
        <CardDescription class="text-center">{{ description }}</CardDescription>
      </CardHeader>
      <CardContent class="grid gap-4">
        <div>
          <p class="text-4xl text-center">$&nbsp;{{ price }}</p>
        </div>
        <div>
          <div
            v-for="(notification, index) in notifications"
            :key="index"
            class="mb-4 grid grid-cols-[25px_minmax(0,1fr)] items-start pb-4 last:mb-0 last:pb-0"
          >
            <span class="flex h-2 w-2 translate-y-1 rounded-full bg-sky-500" />
            <div class="space-y-1">
              <p class="text-sm font-medium leading-none">
                {{ notification.title }}
              </p>
            </div>
          </div>
        </div>
      </CardContent>
      <CardFooter>
        <Button class="w-full uppercase">
          <Check class="mr-2 h-4 w-4" /> Select this plan
        </Button>
      </CardFooter>
    </Card>
  </div>
</template>

<script setup>
import { Check } from "lucide-vue-next";

import { Button } from "@/components/ui/button";
import {
  Card,
  CardContent,
  CardDescription,
  CardFooter,
  CardHeader,
  CardTitle,
} from "@/components/ui/card";

defineProps({
  title: {
    type: String,
    required: true,
  },
  description: {
    type: String,
    required: true,
  },
  price: {
    type: Number,
    required: true,
  },
});

const notifications = [
  {
    title: "Your call has been confirmed.",
  },
  {
    title: "You have a new message!",
  },
  {
    title: "Your subscription is expiring soon!",
  },
];
</script>
