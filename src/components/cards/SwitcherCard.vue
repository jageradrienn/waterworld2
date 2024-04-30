<template>
    <section class=" flex justify-between items-center relative gap-8">
        <Switcher />
        <Svg :src="'../components/icons/Settings.vue'" />
    </section>
</template>

<script setup>
import Svg from '../Svg.vue';
import Switcher from '../Switcher.vue'
</script>

<style scoped></style>