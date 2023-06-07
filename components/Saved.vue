<script setup>
    const { el } = defineProps(['el'])
    console.log(el);
</script>


<template>
    <img class="mb-[12px]" :src="'/' + el.img" width="100%" alt="">
    <h1 class="font-semibold text-[20px] mb-[12px]">${{ el.price }}</h1>
    <h1 class="w-[240px] text-[#606060] text-[18px] mb-[15px]">{{ el.title }}</h1>
    <button class="border-[1px] border-[#DEE2E7] rounded-[6px] py-[14px] px-[19px] flex items-center gap-[7.5px] text-[#0D6EFD] hover:bg-[#0D6EFD] duration-300 hover:text-white"><i class='bx bx-cart text-[23px]' ></i> Move to cart</button>
</template>


<style lang="scss" scoped>

</style>