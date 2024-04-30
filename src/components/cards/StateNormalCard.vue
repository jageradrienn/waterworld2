<template>
    <div class="selector flex items-center justify-center min-w-[160px] h-[160px]">
        <p class=" text-4xl text-nowrap text-center w-full">{{ label }}</p>
    </div>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
    label: String,
})
</script>

<style scoped>
.selector {
    box-shadow: 1px 1px 1px 0px rgba(255, 251, 235, 0.30) inset, -1px -1px 1px 0px rgba(149, 134, 83, 0.50) inset, -2px 2px 5px 0px rgba(149, 134, 83, 0.20), 2px -2px 5px 0px rgba(149, 134, 83, 0.20), 2px 2px 5px 0px rgba(149, 134, 83, 0.20);
    @apply bg-yellow-50 py-5 px-6
}
</style>