<template>
  <div>
    <Suspense v-if="showLazyLoadedComonent">
      <template #default>
        <AsyncComponent />
      </template>
      <template #fallback>
        <Spinner />
      </template>
    </Suspense>
    <button
      @click="showLazyLoadedComonent = true"
      class="bg-blue-500 block m-auto p-2 rounded-md text-white mt-6"
    >
      Show
    </button>
  </div>
</template>

<script setup lang="ts">
  import { defineAsyncComponent, ref } from 'vue'
  import Spinner from '@/components/Spinner.vue'

  const showLazyLoadedComonent = ref(false)

  const AsyncComponent = defineAsyncComponent({
    loader: () => import('../components/LazyLoadedComponent.vue'),
  })
</script>
