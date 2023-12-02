<script setup lang="ts">
const route = useRoute<'hi-id'>()
const user = useUserStore()
const name = route.params.id

watchEffect(() => {
  user.setNewName(route.params.id as string)
})
</script>

<template>
  <div class="flex items-center flex-col gap-4">
    <div class="i-twemoji-waving-hand inline-block animate-shake-x animate-duration-5000 text-4xl" />
    <h3 class="text-2xl font-semibold">
      Hi,
    </h3>
    <div class="text-xl">
      {{ name }}!
    </div>
    <template v-if="user.otherNames.length">
      <div class="my-4 text-sm">
        <span op-50>Also as known as:</span>
        <ul>
          <li v-for="otherName in user.otherNames" :key="otherName">
            <router-link :to="`/hi/${otherName}`" replace>
              {{ otherName }}
            </router-link>
          </li>
        </ul>
      </div>
    </template>
    <Counter />
    <div>
      <NuxtLink
        class="m-3 text-sm btn"
        to="/"
      >
        Back
      </NuxtLink>
    </div>
  </div>
</template>
