<script setup>
    const { service } = defineProps(['service'])
    console.log(service)
</script>


<template>
    <div class="h-[120px]" :class="service.className"></div>
    <i :class="service.icon"
        class='absolute xl:mt-[-30px] mt-[-25px] sm:mt-[-30px] md:ml-[300px] lg:mt-[-20px] ml-[230px] sm:ml-[240px] 2xl:ml-[295px] xl:ml-[235px] lg:ml-[187px] hover:bg-white hover:border-gray-300 hover:cursor-pointer duration-300 text-right text-[26px] lg:p-[8px] xl:p-[16px] sm:p-[16px] p-[10px] bg-[#D1E7FF] border-[2px] border-white rounded-full'></i>
    <div class="py-[18px] px-[22px] bg-white">
        <h1 class="w-[200px] text-[18px] font-medium">{{ service.title }}</h1>
    </div>
</template>


<style lang="scss" scoped>

.hubs{
    background-image: url("../public/Hubs.png");
    background-size: cover;
    background-repeat: no-repeat;
}

.custom{
    background-image: url("../public/Custom.png");
    background-size: cover;
    background-repeat: no-repeat;
}

.shipping{
    background-image: url("../public/Shipping.png");
    background-size: cover;
    background-repeat: no-repeat;
}

.monitoring{
    background-image: url("../public/Monitoring.png");
    background-size: cover;
    background-repeat: no-repeat;
}

</style>