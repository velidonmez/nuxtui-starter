<script setup lang="ts">
import { appName } from '~/constants'

useHead({
  title: appName,
})
</script>

<template>
  <VitePwaManifest />
  <UNotifications />
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>
