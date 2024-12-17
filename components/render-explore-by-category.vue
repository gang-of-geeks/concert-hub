<script lang="ts" setup>
interface props {
  values: {
    image: string
  }
  overlay: string
}
const props = defineProps<props>()
</script>

<template>
  <div class="image w-60 h-56 rounded-xl overflow-hidden mt-5 relative">
    <NuxtImg :src="values.image" class="w-full h-full object-cover" />
    <div
      class="overlay absolute content-none top-0 left-0 w-full h-full bg-black opacity-50 z-10"
    >
      <h1 class="text-white z-20 relative">{{ overlay }}</h1>
    </div>
  </div>
</template>
