<script setup lang="ts">
import Header from '~/components/layout/header.vue';
import Footer from '~/components/layout/footer.vue';
</script>

<template>
  <div>
    <Header />
    <slot />
    <Footer />
  </div>
</template>
