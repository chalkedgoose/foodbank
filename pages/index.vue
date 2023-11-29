<script setup lang="ts">
const { $client } = useNuxtApp()

const hello = await $client.hello.useQuery({ text: 'client' })
</script>

<template>
  <div class="flex items-center justify-center max-w-5xl outline-neutral-800 outline-1 outline-dashed">
    <p>{{ hello.data?.value?.greeting }}</p>
    <UiButton variant="outline">Close on Index</UiButton>
  </div>
</template>
