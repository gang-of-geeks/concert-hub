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
      class="overlay absolute content-none bottom-0 left-0 w-full h-12  render-explore-bu-category-cutomBackground z-10"
    >
  </div>
    <h1 class="text-white bottom-3 text-xl font-normal left-1/2 transform -translate-x-1/2 absolute  z-20 text-center">{{ overlay }}</h1>
  </div>
</template>
