<script setup>
    const { i } = defineProps(["i"])
    console.log(i);
</script>


<template>
    <img :src="'/' + i.img" class="mr-[15px] w-[40px] h-[26px]" alt="">
    <div>
        <h1 class="text-[18px]">{{ i.country }}</h1>
        <h1 class="text-[15px] text-[#8B96A5] hover:cursor-pointer">{{ i.site }}</h1>
    </div>
</template>


<style lang="scss" scoped></style>