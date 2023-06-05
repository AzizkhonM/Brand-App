<script setup>

    const { card } = defineProps(["card"])
    console.log(card);

</script>


<template>
    <div class="h-[155px] pt-[15px] pl-[18px] pb-[10px] border rounded-[6px] hover:cursor-pointer">
        <div class="mb-[12px]">
            <h1 class="xl:text-[24px] text-[11px] lg:text-[16px] md:text-[8px] hometitle">{{ card.product }}</h1>
        </div>
        <div class="flex justify-between card">
            <h1 class="lg:text-[19px] text-[8px] text-[#8B96A5] homeprice">From ${{ card.price }}</h1>
            <img :src="card.img" alt="" style="margin-right: 10px; margin-bottom: 10px;">
        </div>
    </div>
</template>


<style lang="scss" scoped>

@media screen and (max-width: 600px) {
.hometitle{
        font-size: 16px;
    }

    .homeprice{
        font-size: 15px;
    }
}

</style>