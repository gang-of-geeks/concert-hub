<script lang="ts" setup>
import Subjects from './subjects.vue';
import Swiper from './swiper/swiper.vue';
import  {Navigation} from "swiper/modules"

interface Props {
  values: {
    image: string
  }[]
  subject: string
}
defineProps<Props>()
</script>

<template>
    <div class="artist">
        <Subjects :subject="subject"/>
        <div class="swiper">
            <Swiper direction="horizontal" :modules="[Navigation]" :values="values" :navigation="true"/>
        </div>
    </div>
</template>