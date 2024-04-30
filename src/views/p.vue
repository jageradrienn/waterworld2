<template>
    <div class="w-full px-[112px] py-8 flex flex-col justify-center gap-8">
        <div class="flex items-center gap-8">
            <p class="text-4xl">Mellények</p>
            <Svg :src="data.mstatus === 'free' ? '../components/icons/BlueDot.vue'
                : data.mstatus === 'reserved' ? '../components/icons/OrangeDot.vue'
                    : (data.mstatus === 'reserved') && data.isClosed ? '../components/icons/RedDot.vue' : data.mstatus === 'wrong' ? '' : null"
                class="w-[16px] h-[16px]" />
            <p class="text-4xl">{{ data.mlabel }}</p>

        </div>
        <div class="flex items-center gap-8">
            <MellenyCard :mstatus="data.mstatus" :mstatusLabel="data.mstatusLabel" :mlabel="data.mlabel"
                :msize="data.msize" :order="data.order" :time="data.time" :warning="data.warning"
                :isClosed="data.isClosed" class="mt-16" />
            <article class="right-card p-[112px]">
                <p class="text-4xl leading-[120%]">Válassz csomagot!</p>
                <p class="leading-[152%] mb-8">Válaszd ki, hogy melyik csomaggal szeretnéd kiadni a mellényt.</p>
                <div class="flex items-center gap-5">
                    <StateNormalCard label="10perc" />
                </div>
            </article>
        </div>
    </div>
</template>

<script setup>
import MellenyCard from '../components/cards/MellenyCard.vue';
import Svg from '../components/Svg.vue';
import StateNormalCard from '../components/cards/StateNormalCard.vue';

const props = defineProps({
    data: {
        type: Object,
        required: true
    }
})
</script>

<style scoped></style>