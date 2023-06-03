<script setup>
import { headerCurrencies } from '../../constants/headerCurrencies';
import { headerCountries } from "../../constants/headerCountries"
</script>


<template>
    <div class="border border-b-[2px]">
        <div class="mx-auto container" style="font-family: 'Inter'">
            <div class="flex items-center justify-between">
                <div class="grid grid-cols-6 gap-[25px] items-center font-medium">
                    <div class="text-[16px]">All category</div>
                    <div class="text-[16px]">Hot offers</div>
                    <div class="text-[16px]">Gift boxes</div>
                    <div class="text-[16px]">Projects</div>
                    <div class="text-[16px]">Menu item</div>
                    <div class="text-[16px]">
                        <select name="" id="" class="bg-white outline-none border-none hover:cursor-pointer">
                            <option value="">Help</option>
                        </select>
                    </div>
                </div>
                <div>
                    <select name="currencies" id="" class="bg-white outline-none border-none font-medium hover:cursor-pointer">
                        <option v-for="el in headerCurrencies" :value="el.title">{{ el.title }}</option>
                    </select>
                    <select name="countries" id="" class="bg-white outline-none border-none font-medium hover:cursor-pointer">
                        <option  v-for="el in headerCountries" :value="el.title">{{ el.title }}</option>
                    </select>
                </div>
            </div>
        </div>
    </div>
</template>


<style lang="scss" scoped>

</style>