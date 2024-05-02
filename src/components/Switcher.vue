<template>
    <section class="switcher relative">
        <div class="absolute switcher-bg top-0 left-1 w-full h-full ">
            <div class="relative flex justify-between items-center h-full  ">
                <div class="flex items-center gap-2 ml-8 ">
                    <ActiveBlue /><span class="text-lg text-Blue-400 text-center">Aktív</span>
                </div>
                <div class="flex items-center gap-2 mr-12">
                    <BreakBrown /><span class="text-lg text-Brown text-center">Szüneteltetve</span>
                </div>
            </div>
            <div class="absolute -top-2 left-0 ">
                <div class="relative">
                    <NormalOvalBTNCream class="w-[185px]" />
                    <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 flex items-center gap-2">
                        <ActiveBlue />
                        <p class=" text-lg text-Blue-400 text-center">
                            Aktív</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>

import ActiveBlue from './icons/ActiveBlue.vue';
import BreakBrown from './icons/BreakBrown.vue';
import NormalOvalBTNCream from './icons/NormalOvalBTNCream.vue';
</script>

<style scoped>
.switcher-bg {
    box-shadow: 5px 5px 4px 0px rgba(149, 134, 83, 0.20) inset, -5px -5px 4px 0px rgba(255, 251, 235, 0.30) inset;
    border: 1px solid rgba(255, 255, 255, 0.05);
    @apply bg-Yellow-100 rounded-[50px]
}
</style>