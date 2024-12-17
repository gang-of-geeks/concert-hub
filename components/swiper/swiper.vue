<script setup lang="ts">
import { Swiper, SwiperSlide } from 'swiper/vue'



interface props {
  direction: "horizontal" | "vertical",
  swiperSlideClass?: string
  modules: any[],
  values: {
    image: string
  }[]
}
defineProps<props>()
</script>

<template>
  <Swiper
    :direction="direction"
    :pagination="{
      clickable: true,
    }"
    :modules="modules"
    :loop="true"
  >
    <SwiperSlide
      v-for="(items, key) in values"
      :key="key"
      :class="swiperSlideClass"
    >
      <NuxtImg :src="items.image" class="h-full w-full object-cover" />
    </SwiperSlide>
  </Swiper>
</template>
