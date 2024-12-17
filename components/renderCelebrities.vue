<script setup lang="ts">
interface Props {
  values: {
    image: string
  }
}
defineProps<Props>()
</script>

<template>
  <div
    class="celebrities-info w-72 rounded-xl overflow-hidden mt-5 mb-5 shrink-0 pb-3"
  >
    <div class="celebrities-image">
      <NuxtImg
        :src="values.image"
        class="w-full h-72 object-cover rounded-xl"
      />
    </div>
    <div class="info flex justify-center items-center flex-col">
      <div class="celebrities-name text-2xl font-normal mb-1 z-10">lalala</div>
      <div class="celebrities-location font-semibold">Canada</div>
      <div class="celebrities-date font-semibold">24 may 2:00:00</div>
    </div>
  </div>
</template>
<style scoped>
.celebrities-info {
  border: 1px solid #d1d1d7;
}
.celebrities-info .celebrities-name {
  color: #282831;
}
.celebrities-info .celebrities-image {
  position: relative;
  z-index: 2;
}
.celebrities-info .celebrities-image::after {
  content: '';
  position: absolute;
  bottom: -32px;
  left: 0;
  width: 100%;
  height: 20%;
  background: linear-gradient(to bottom , #0000001e , #00000017 ,#0000001c ,   #fff );
  z-index: -1;
}
.celebrities-info :is(.celebrities-date, .celebrities-location) {
  color: #3d3d49;
}
</style>
