<template>
    <article class="right-card px-[112px] py-[84px] flex flex-col gap-8">
        <HeadingCard h1Label="Válassz csomagot!"
            h2Label="Válaszd ki, hogy melyik csomaggal szeretnéd kiadni a mellényt." />
        <PackagesCard />
        <BtnCard src="./icons/ArrowBlueLeft.vue" inactiveLabel="Vissza" activeLabel="Kiadom" active="true"
            class="pt-4" />
        <HeadingCard h1Label="Státusz módosítása" h2Label="Szüneteltetheted a mellény kiadását." class="pt-12" />
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