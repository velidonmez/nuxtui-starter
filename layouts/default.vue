<script setup lang="ts">
</script>

<template>
  <LayoutHeader />
  <main class="min-h-[calc(100vh-var(--header-height))]">
    <UContainer>
      <slot />
    </UContainer>
  </main>
  <LayoutFooter />
</template>
