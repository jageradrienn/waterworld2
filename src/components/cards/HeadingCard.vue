<template>
    <p class="text-4xl leading-[120%]">{{ h1Label }}</p>
    <p class="leading-[152%] mb-8">{{ h2Label }}</p>
</template>

<script setup>
defineProps({
    h1Label: String,
    h2Label: String,
})
</script>

<style lang="scss" scoped></style>