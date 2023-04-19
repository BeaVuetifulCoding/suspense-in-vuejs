<template>
  <header>
    <div class="wrapper">
      <nav class="flex justify-center">
        <RouterLink class="p-3" to="/">Home</RouterLink>
        <RouterLink class="p-3" to="/about">About</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView v-slot="{ Component }">
    <Transition name="fade" mode="out-in">
      <KeepAlive>
        <component :is="Component" />
      </KeepAlive>
    </Transition>
  </RouterView>
</template>

<script setup lang="ts">
  import { RouterLink, RouterView } from 'vue-router'
</script>

<style scoped>
  a {
    @apply font-bold;
  }

  a.router-link-exact-active {
    @apply text-vue-green underline;
  }

  .fade-enter-active,
  .fade-leave-active {
    transition: opacity 0.5s ease;
  }

  .fade-enter-from,
  .fade-leave-to {
    opacity: 0;
  }
</style>
