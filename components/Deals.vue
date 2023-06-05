<script setup>
/* v-for="el in offers" :key="el.id"  */
const { offer } = defineProps(["offer"])
console.log(offer);
</script>


<template>
    <div class="border-x-[1px] rounded-[6px] p-[13px] hover:cursor-pointer">
        <div class="mb-[13px] flex justify-center"><img :src="offer.img" alt=""></div>
        <h1 class="mb-[10px] text-center">{{ offer.product }}</h1>
        <div class="flex justify-center">
            <h1 class="bg-[#FFE3E3] text-[#EB001B] font-medium py-[7px] px-[15px] rounded-full text-center w-[65px]">-{{
                offer.percent }}%</h1>
        </div>
    </div>
</template>


<style lang="scss" scoped></style>