<script setup>
const { phone } = defineProps(['phone'])
console.log(phone);
</script>


<template>
    <div class="bg-white rounded-[6px] grid grid-cols-1 hover:cursor-pointer">
        <div class="flex justify-center border-b-[1px]"><img height="260" width="260" :src="phone" alt=""></div>
        <div class="py-[20px] px-[22px]" style="display: grid; grid-template-columns: 70% 30%;">
            <div>
                <div class="flex justify-start items-center gap-[10px] mb-[11px]">
                    <h1 class="text-[20px] font-bold">$99.50</h1>
                    <h2 class="text-[18px] text-[#8B96A5] line-through">$1128.00</h2>
                </div>
                <n-rate readonly :default-value="4" class="mb-[12px]" />
                <h1 class="text-[18px] text-[#606060]">GoPro HERO6 4K Action Camera - Black</h1>
            </div>
            <div class="flex justify-end items-start">
                <button
                    class="border-[1px] border-[#DEE2E7] rounded-[6px] p-[10px] flex justify-center items-center text-[#0D6EFD] hover:bg-[#0D6EFD] hover:text-white duration-300"><i
                        class='bx bx-heart text-[26px]'></i></button>
            </div>
        </div>
    </div>
</template>


<style lang="scss" scoped></style>