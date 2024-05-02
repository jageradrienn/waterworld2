<template>
    <article class="flex items-center gap-8">
        <button v-if="inactive === 'true'" class="btn-inactive flex items-center justify-center " :class="size">
            <Svg v-if="src" :src="src" /><span class="text-2xl text-Blue-400 text-center ml-2">{{ inactiveLabel
                }}</span>
        </button>
        <button v-if="active === 'true'" class="btn-active" :class="size">
            <span class="text-2xl text-white text-center w-full">{{ activeLabel }}</span>
        </button>
    </article>
</template>

<script setup>
import { stringify } from 'postcss';
import Svg from '../Svg.vue';
import { defineProps } from 'vue';
defineProps({
    activeLabel: String,
    inactiveLabel: String,
    src: String,
    active: String,
    inactive: String,
    size: String,
})
</script>

<style scoped></style>