<template>
  <div>
    <h1 v-if="showResolvedMessage" class="bg-green-500 text-white text-center">
      Data successfylly fetched from the server
    </h1>
    <h2 v-if="showPendingMessage" class="bg-blue-500 text-white text-center">
      Pending State...
    </h2>
    <h3 class="text-center font-bold">Fallback Example</h3>
    <h4 v-if="errorMessage" class="font-bold text-3xl text-red-500 text-center">
      {{ errorMessage }}
    </h4>
    <Suspense
      @pending="pendingMethod"
      @resolve="resolveMethod"
      @fallback="fallbackMethod"
    >
      <template #default>
        <Todos />
      </template>
      <template #fallback>
        <Spinner />
      </template>
    </Suspense>
  </div>
</template>

<script setup lang="ts">
  import { ref, onErrorCaptured } from 'vue'
  import Todos from './Todos.vue'
  import Spinner from './Spinner.vue'

  const showResolvedMessage = ref(false)
  const showPendingMessage = ref(false)
  const fallbackColor = ref('black')
  const errorMessage = ref('')

  const pendingMethod = () => {
    console.log('Pending...')
    showPendingMessage.value = true
  }
  const resolveMethod = () => {
    showResolvedMessage.value = true
    setTimeout(() => {
      showResolvedMessage.value = false
    }, 2000)
    showPendingMessage.value = false
    console.log('Resolved')
    fallbackColor.value = 'green'
  }
  const fallbackMethod = () => {
    console.log('Fallback')
    fallbackColor.value = 'red'
  }

  onErrorCaptured((error: Error) => {
    errorMessage.value = error.message
    return false
  })
</script>

<style scoped>
  h3 {
    color: v-bind('fallbackColor');
  }
</style>
