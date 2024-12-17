<script setup lang="ts">
import RenderCelebrities from './renderCelebrities.vue'

interface Props {
  values: {
    image: string
  }[]
  subject: string
}
defineProps<Props>()
</script>

<template>
  <div class="together mt-5 mb-12">
    <div class="subject flex justify-between items-center">
      <h1 class="text-2xl">{{ subject }}</h1>
      <h2 class="text-lg">See All</h2>
    </div>
    <div class="celebrities flex justify-between gap-5 overflow-x-auto">
      <RenderCelebrities
        v-for="(items, key) in values"
        :key="key"
        :values="items"
      />
    </div>
  </div>
</template>
<style scoped>

</style>