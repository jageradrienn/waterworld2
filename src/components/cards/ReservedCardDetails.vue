<template>
    <article class="right-card p-[112px] flex flex-col gap-8">
        <HeadingCard h1Label="Státusz módosítása" h2Label="Szüneteltetheted a kiadott mellényt." />
        <Switcher />
        <HeadingCard h1Label="Hosszabbítás" h2Label="Válassz csomagot" />
        <PackagesCard />
        <BtnCard activeLabel="Meghosszabítom" />


    </article>
</template>

<script setup>
import Switcher from '../Switcher.vue';
import BtnCard from './BtnCard.vue';
import HeadingCard from './HeadingCard.vue';
import PackagesCard from './PackagesCard.vue';
</script>

<style scoped></style>