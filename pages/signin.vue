<template>
  <NuxtLayout>
    <div
      class="flex items-center justify-center mx-auto w-[400px] max-h-[500px]"
    >
      <NuxtImg src="/nuxt-clear-english-signin-illustration.png" />
    </div>
    <template #form>
      <div class="flex flex-col items-center justify-center gap-4">
        <div class="text-3xl">
          <h1>Enter Your Credentials</h1>
        </div>
        <div>
          <form action="">
            <div class="flex flex-col">
              <label for="">Conta</label>
              <input type="text" placeholder="Seu email" />
              <label for="">Senha</label>
              <input type="password" placeholder="Sua senha" />
              <label for="">Confirmar Senha</label>
              <input type="password" placeholder="Confirmar a senha" />
            </div>
          </form>
        </div>
      </div>
    </template>
  </NuxtLayout>
</template>

<script lang="ts" setup>
useHead({
  title: "Sign In",
});

definePageMeta({
  layout: "auth",
});
</script>
