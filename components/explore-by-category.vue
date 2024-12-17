<script lang="ts" setup>
import RenderExploreByCategory from './render-explore-by-category.vue';

interface Props {
  values: {
    image: string
  }[]
  subject: string
}
defineProps<Props>()
</script>

<template>
    <div class="explore-by-category">
        <div class="subject">
            <h1 class="text-2xl">{{ subject }}</h1>
        </div>
        <div class="renderExplore flex justify-between gap-5 overflow-x-auto">
            <RenderExploreByCategory v-for="(items, key) in values" :key="key" :values="items" overlay="hihihi" />
        </div>
    </div>
</template>