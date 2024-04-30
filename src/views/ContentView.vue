<script setup>
import MellenyCard from '../components/cards/MellenyCard.vue';
import NoClosedCard from '../components/cards/NoClosedCard.vue';
import Homokora from '../components/icons/Homokora.vue';
import ClosedCard from '../components/cards/ClosedCard.vue';
import { ref, onMounted } from 'vue';
import { RouterLink } from 'vue-router'
import { defineProps } from 'vue';

const props = defineProps({
    MellenyDetails: {
        type: Array,
        default: () => []
    },
    fullData: Number,
})


</script>

<template>

    <section class="content flex justify-center items-center pt-[25px] gap-[52px]">
        <article class="flex flex-col gap-8">
            <div class="flex justify-between items-center">
                <p class="text-4xl ml-8">Mellények</p>
                <p class="text-4xl mr-8"><span>{{ fullData }}</span>/<span>{{ MellenyDetails.length }} </span> Elérhető
                </p>
            </div>
            <div class="left-blur-card flex justify-between items-center ">
                <div class="gridBox h-full w-[97%] pt-20 pl-7 pr-[60px] grid grid-cols-4 gap-x-5 gap-y-16 "
                    :class="MellenyDetails.length ? 'overflow-y-auto' : null">
                    <template v-for="item in MellenyDetails" :key="item.id">
                        <RouterLink to="/packages" target="_blank">
                            <MellenyCard :mstatus="item.mstatus" :mstatusLabel="item.mstatusLabel" :mlabel="item.mlabel"
                                :msize="item.msize" :order="item.order" :time="item.time" :warning="item.warning"
                                :isClosed="item.isClosed" />
                        </RouterLink>

                    </template>
                </div>
            </div>
        </article>
        <article class="right-blur-card ">
            <div class="flex flex-col items-center justify-center gap-6">
                <Homokora />
                <p class="text-4xl font-bold">Lejárt mellények</p>
                <NoClosedCard />
            </div>
            <div class="flex flex-col items-center justify-center gap-6">
                <template v-for="item in MellenyDetails" :key="item.id">
                    <ClosedCard v-if="item.isClosed" :mlabel="item.mlabel" />
                </template>
            </div>

        </article>
    </section>

</template>

<style scoped>
.gridBox::-webkit-scrollbar {
    width: 18px;
}

.gridBox::-webkit-scrollbar-track {
    margin-top: 32px;
    margin-bottom: 32px;
    border-radius: 12px;
    background-color: #FFFBEB;
    border: 2px solid white;
    box-shadow: -1px -1px 3px 0px #FFF, 1.5px 1.5px 3px 0px rgba(174, 174, 192, 0.40);
}

.gridBox::-webkit-scrollbar-thumb {
    width: 16px;
    border-radius: 12px;
    background-image: linear-gradient(90deg, #1EBAFF 100%, #127099 0%);
    box-shadow: 0px 0px 2px 0px rgba(114, 138, 183, 0.70);
}
</style>
