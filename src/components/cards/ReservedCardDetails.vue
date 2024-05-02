<template>
    <article class="right-card px-[112px] h-[796px] flex flex-col justify-center gap-8">
        <HeadingCard h1Label="Státusz módosítása" h2Label="Szüneteltetheted a kiadott mellényt." />
        <Switcher />
        <HeadingCard h1Label="Hosszabbítás" h2Label="Válassz csomagot!" />
        <PackagesCard />
        <div class="flex items-center gap-8 mt-4 ">
            <BtnCard src="./icons/ArrowBlueLeft.vue" inactive="true" inactiveLabel="Vissza" size="short" />
            <BtnCard activeLabel="Meghosszabbítom" active="true" size="wide" />
        </div>
    </article>
</template>

<script setup>
import PackagesCard from './PackagesCard.vue';
import HeadingCard from './HeadingCard.vue';
import Switcher from '../Switcher.vue';
import BtnCard from './BtnCard.vue';
import Svg from '../Svg.vue';
</script>

<style scoped>
.delivered {
    background-image: linear-gradient(#FFFBEB, #FDF1C8) !important;
    box-shadow: -2px -2px 4px 0px rgba(149, 134, 83, 0.10) inset, 2px 2px 4px 0px #FFFBEB inset, -5px -5px 5px 0px rgba(255, 251, 235, 0.40), 5px 5px 10px 0px rgba(149, 134, 83, 0.20);
    border: 2px solid rgba(0, 0, 0, 0.05);
    width: 317px;
    height: 128px;
    @apply opacity-90 rounded-[50px] px-16 py-12 mt-12
}
</style>