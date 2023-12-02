<script setup lang="ts">
const online = useOnline()
const toast = useToast()
</script>

<template>
  <div class="flex flex-col justify-center items-center w-full gap-4">
    <Logos />
    <Suspense>
      <ClientOnly>
        <UButton
          label="Show toast"
          @click="toast.add({ title: 'Hello world!' })"
        />
        <PageView v-if="online" />
        <div v-else class="text-gray-80">
          You're offline
        </div>
      </ClientOnly>
      <template #fallback>
        <div class="italic opacity-50">
          <span animate-pulse>Loading...</span>
        </div>
      </template>
    </Suspense>
    <InputEntry />
  </div>
</template>
