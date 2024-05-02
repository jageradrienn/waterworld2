<template>
    <div>
        <p class="text-4xl">{{ h1Label }}</p>
        <p>{{ h2Label }}</p>
    </div>
</template>

<script setup>
defineProps({
    h1Label: String,
    h2Label: String,
})
</script>

<style lang="scss" scoped></style>