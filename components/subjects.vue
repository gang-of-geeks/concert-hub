<script setup lang="ts">

interface props {
    subject: string
}

defineProps<props>()
</script>
<template>
    <div class="subject">
            <h1 class="text-2xl">{{ subject }}</h1>
    </div>
</template>