<template>
    <div class="w-full pl-[112px] py-8 flex flex-col justify-center gap-8">
        <div class="flex items-center gap-8">
            <p class="text-4xl">Mellények</p>
            <!-- <Svg :src="status === 'free' ? '../components/icons/BlueDot.vue'
                : status === 'reserved' ? '../components/icons/OrangeDot.vue'
                    : (status === 'reserved') && isClosed ? '../components/icons/RedDot.vue'
                        : status === 'wrong' ? '' : null" class="w-[16px] h-[16px]" /> -->
            <Svg :src="loadStatusDot()" class="w-[16px] h-[16px]" />
            <p class="text-4xl">{{ label }}</p>

        </div>
        <div class="flex items-center gap-8">
            <MellenyCard :status="status" :statusLabel="statusLabel" :label="label" :size="size" :order="order"
                :time="time" :warning="warning" :isClosed="isClosed" class="mt-16" />

            <FreeCardDetails v-if="status === 'free'" />
            <ReservedCardDetails v-if="status === 'reserved'" />
        </div>
    </div>
</template>

<script setup>
import MellenyCard from '../components/cards/MellenyCard.vue';
import Svg from '@/components/Svg.vue';
import FreeCardDetails from '@/components/cards/FreeCardDetails.vue';
import ReservedCardDetails from '@/components/cards/ReservedCardDetails.vue';
import StateNormalCard from '@/components/cards/StateNormalCard.vue';
const props = defineProps({
    status: String,
    statusLabel: String,
    label: String,
    size: String,
    order: String,
    time: String,
    warning: Boolean,
    isClosed: Boolean,
})

const loadStatusDot = () => {
    let components = {
        free: '../components/icons/BlueDot.vue',
        reserved: '../components/icons/OrangeDot.vue',
        expired: '../components/icons/RedDot.vue',
        wrong: '',
    }

    if (props.status === 'reserved' && props.isClosed) {
        return components['expired']
    }

    return components[props.status]
}

</script>

<style scoped></style>