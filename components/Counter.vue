<script setup lang='ts'>
const { count, inc, dec } = useCount()
</script>

<template>
  <div class="flex gap-2">
    <UButton
      :ui="{ rounded: 'rounded-full' }"
      size="xs"
      variant="soft"
      icon="i-carbon-subtract"
      @click="dec()"
    />
    <div class="m-auto inline-block">
      {{ count }}
    </div>
    <UButton
      icon="i-carbon-add"
      size="xs"
      variant="soft"
      :ui="{ rounded: 'rounded-full' }"
      @click="inc()"
    />
  </div>
</template>
