<script lang="ts" setup>
import RenderExploreByCategory from './render-explore-by-category.vue';
import Subjects from './subjects.vue';

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
          <Subjects :subject="subject"/>
        <div class="renderExplore flex justify-between gap-5 overflow-x-auto">
            <RenderExploreByCategory v-for="(items, key) in values" :key="key" :values="items" overlay="hihihi" />
        </div>
    </div>
</template>