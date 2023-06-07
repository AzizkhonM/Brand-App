<script setup>
    const { el } = defineProps(['el'])
    console.log(el);
</script>


<template>
    <img :src="'/' + el + '.png'" width="45" height="30" alt="">
</template>


<style lang="scss" scoped>

</style>