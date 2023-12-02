<template>
  <header class="bg-background/75 backdrop-blur border-b -mb-px sticky top-0 z-50 border-gray-200 dark:border-gray-800">
    <UContainer>
      <div class="h-16 flex justify-between items-center">
        <nuxt-link to="/">
          Logo
        </nuxt-link>
        <nav class="flex justify-between gap-4">
          <nuxt-link to="/">
            Nav#1
          </nuxt-link>
          <nuxt-link to="/">
            Nav#2
          </nuxt-link>
          <nuxt-link to="/">
            Nav#3
          </nuxt-link>
        </nav>
        <div class="flex justify-center items-center">
          <DarkToggle />
        </div>
      </div>
    </UContainer>
  </header>
</template>
