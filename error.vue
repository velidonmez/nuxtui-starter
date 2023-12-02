<script setup>
defineProps({
  error: Object,
})

const handleError = () => clearError({ redirect: '/' })
</script>

<template>
  <main class="flex items-center justify-center h-[calc(100vh-8rem)]">
    <div class="p-4 space-y-4">
      <div class="flex flex-col items-start space-y-3 sm:flex-row sm:space-y-0 sm:items-center sm:space-x-3">
        <p class="font-semibold text-red-500 text-9xl">
          {{ error.statusCode }}
        </p>
        <div class="space-y-2">
          <h1 id="pageTitle" class="flex items-center space-x-2">
            <span class="i-heroicons-solid-exclamation-circle w-8 h-8 text-red-500" />
            <span class="text-xl font-medium text-gray-600 sm:text-2xl">
              Oops!
            </span>
          </h1>
          <p class="text-base font-normal text-gray-600 dark:text-gray-300">
            {{ error.statusMessage }}
          </p>
          <p class="text-base font-normal text-gray-600 dark:text-gray-300">
            You may return to
            <button class="text-blue-600 hover:underline dark:text-blue-500" @click="handleError">
              home page
            </button>.
          </p>
        </div>
      </div>
    </div>
  </main>
</template>
