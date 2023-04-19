<template>
  <div>{{ data }}</div>
</template>

<script setup lang="ts">
  //   const response = await fetch('https://jsonplaceholder.typicode.com/todos/')
  //   const data = await response.json()

  const data = await(
    await fetch('https://jsonplaceholder.typicode.com/todos/')
  ).json()
</script>
