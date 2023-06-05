<script setup>
import { headerCurrencies } from '../../constants/headerCurrencies';
import { headerCountries } from "../../constants/headerCountries"
</script>


<template>
    <div class="border border-b-[2px]">
        <div class="mx-auto container" style="font-family: 'Inter'">
            <div class="flex items-center justify-between headerr">
                <div class="grid things grid-cols-6 gap-[25px] items-center font-medium">
                    <div class="xl:text-[16px] flex items-center sm:text-[8px] lg:text-[12px] hover:cursor-pointer">All category</div>
                    <div class="xl:text-[16px] flex items-center sm:text-[8px] lg:text-[12px] hover:cursor-pointer">Hot offers</div>
                    <div class="xl:text-[16px] flex items-center sm:text-[8px] lg:text-[12px] hover:cursor-pointer">Gift boxes</div>
                    <div class="xl:text-[16px] flex items-center sm:text-[8px] lg:text-[12px] hover:cursor-pointer">Projects</div>
                    <div class="xl:text-[16px] flex items-center sm:text-[8px] lg:text-[12px] hover:cursor-pointer">Menu item</div>
                    <div class="xl:text-[16px] flex items-center sm:text-[8px] lg:text-[12px] hover:cursor-pointer">
                        <select name="" id="" class="selects bg-white outline-none border-none hover:cursor-pointer sm:text-[8px] xl:text-[16px] lg:text-[12px]">
                            <option value="">Help</option>
                        </select>
                    </div>
                </div>
                <div>
                    <select name="currencies" id="" class="selects bg-white outline-none border-none font-medium hover:cursor-pointer sm:text-[8px] xl:text-[16px] lg:text-[10px]">
                        <option v-for="el in headerCurrencies" :value="el.title">{{ el.title }}</option>
                    </select>
                    <select name="countries" id="" class="selects bg-white outline-none border-none font-medium hover:cursor-pointer sm:text-[8px] xl:text-[16px] lg:text-[10px]">
                        <option  v-for="el in headerCountries" :value="el.title">{{ el.title }}</option>
                    </select>
                </div>
            </div>
        </div>
    </div>
</template>


<style lang="scss" scoped>

    @media screen and (max-width: 640px) {
        .things{
            display: grid;
            grid-template-columns: 32% 32% 32%;
            font-size: 8px;
            gap: 10px;
            align-items: center;
        }

        .selects{
            font-size: 8px;
        }

        .header{
            padding: 10px 10px -10px 10px;
        }
    }

</style>