<script setup>
    const { card } = defineProps(['card'])
    console.log(card);
</script>


<template>
    <i :class="card.icon"
        class='h-[55px] text-[24px] flex justify-center items-center w-[55px] rounded-full text-[#8B96A5] bg-[#DEE2E7]'></i>
    <div class="grid grid-cols-1 ml-[20px] text-[18px]">
        <h1>{{ card.title }}</h1>
        <h1 class="text-[#A9ACB0]">Have you ever finally just</h1>
    </div>
</template>


<style lang="scss" scoped></style>