<template>
    <article class="flex items-center gap-8">
        <button class="btn-inactive flex items-center justify-center ">
            <Svg :src="src" /><span class="text-2xl text-Blue-400 text-center">{{ inactiveLabel }}</span>
        </button>
        <button v-if="active" class="btn-active">
            <span class="text-2xl text-white text-center w-full">{{ activeLabel }}</span>
        </button>
    </article>
</template>

<script setup>
import Svg from '../Svg.vue';
import ArrowBlueLeft from '../icons/ArrowBlueLeft.vue';
import { defineProps } from 'vue';
defineProps({
    activeLabel: String,
    inactiveLabel: String,
    src: String,
    active: Boolean,
})
</script>

<style scoped></style>