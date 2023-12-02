<script setup lang="ts">
const name = ref('')

const router = useRouter()
function go() {
  if (name.value)
    router.push(`/hi/${encodeURIComponent(name.value)}`)
}
</script>

<template>
  <div class="flex justify-center flex-col gap-4 w-1/2">
    <UInput
      id="input"
      v-model="name"
      placeholder="What's your name?"
      type="text"
      autocomplete="off"
      @keydown.enter="go"
    />
    <div>
      <UButton
        :disabled="!name"
        @click="go"
      >
        GO
      </UButton>
    </div>
  </div>
</template>
