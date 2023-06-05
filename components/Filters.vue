<script setup>
    const { filter } = defineProps(["filter"])
    console.log(filter);
</script>


<template>
    <div class="flex items-center px-[12px] py-[8px] text-[18px] gap-[11px] border-[1px] border-[#0d6efd] rounded-[6px] bg-white">{{ filter }} <i class='bx bx-x hover:cursor-pointer'></i></div>
</template>


<style lang="scss" scoped>

</style>