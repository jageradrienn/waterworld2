<template>
    <article class="right-card p-[112px]">
        <HeadingCard h1Label="Válassz csomagot!"
            h2Label="Válaszd ki, hogy melyik csomaggal szeretnéd kiadni a mellényt." />
        <PackagesCard />
        <BtnCard activeLabel="Kiadom" />
        <HeadingCard h1Label="Státusz módosítása" h2Label="Szüneteltetheted a mellény kiadását." />
        <Switcher />

    </article>
</template>

<script setup>
import PackagesCard from './PackagesCard.vue';
import HeadingCard from './HeadingCard.vue';
import Switcher from '../Switcher.vue';
import BtnCard from './BtnCard.vue';
</script>

<style scoped></style>