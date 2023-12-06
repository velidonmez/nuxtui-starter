<script setup lang="ts">
const toast = useToast()
</script>

<template>
  <div class="flex flex-col justify-center items-center w-full gap-4">
    <Logos />

    <UButton
      label="Show toast"
      @click="toast.add({ title: 'Hello world!' })"
    />

    <InputEntry />
  </div>
</template>
