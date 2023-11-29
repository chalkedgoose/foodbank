<script setup lang="ts">
const { $client } = useNuxtApp()

const hello = await $client.hello.useQuery({ text: 'client' })
</script>

<template>
  <div>
    <p>{{ hello.data?.value?.greeting }}</p>
  </div>
</template>
