<script setup>
    const { product } = defineProps(['product'])
    console.log(product);
</script>

<template>
    <div class=" max-h-[90px] border-[1px] border-[#DEE2E7] rounded-[10px] p-[7px] flex justify-center items-center">
        <img :src="'/' + product.img" alt="">
    </div>
    <div class="grid grid-cols-1 text-[18px]">
        <h1 class="font-medium text-[#1C1C1C] ">{{ product.title }}</h1>
        <div class="text-[#8B96A5] flex items-center justify-start gap-[25px]">
            <h1>Size: {{ product.size }}</h1>
            <h1>Color: {{ product.color }}</h1>
            <h1>Material: {{ product.material }}</h1>
        </div>
        <h1 class="text-[#8B96A5] mb-[20px]">Seller: {{ product.seller }}</h1>
        <div class="flex items-center gap-[15px]">
            <button
                class="py-[11px] px-[14px] border-[1px] border-[#DEE2E7] rounded-[6px] text-[#FA3434] hover:bg-[#FA3434] hover:text-white duration-300 hover:cursor-pointer">Remove</button>
            <button
                class="py-[11px] px-[14px] border-[1px] border-[#DEE2E7] rounded-[6px] text-[#0D6EFD] hover:bg-[#0D6EFD] hover:text-white duration-300 hover:cursor-pointer">Save
                for later</button>
        </div>
    </div>
    <div class="grid grid-cols-1  w-[85%]">
        <div class="flex justify-end">
            <h1 class="font-medium text-[18px]">${{ product.price }}</h1>
        </div>
        <sproductelect class="border-[1px] border-[#DEE2E7] rounded-[6px] py-[13px] px-[12px] h-[52px] w-auto" name="" id="">
            <option value="">Qty: {{ product.quantity }}</option>
        </sproductelect>
    </div>
</template>


<style lang="scss" scoped></style>