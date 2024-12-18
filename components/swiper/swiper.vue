<script setup lang="ts">
import { Swiper, SwiperSlide } from 'swiper/vue'
import 'swiper/css/navigation';
import 'swiper/css'
import 'swiper/css/pagination'

interface props {
  direction: "horizontal" | "vertical",
  swiperSlideClass?: string
  navigation?: boolean
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
    :navigation="navigation"
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
