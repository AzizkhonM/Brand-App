<script setup>
import { footerLanguages } from "../../constants/footerLanguages"
import { about } from "../../constants/about"
import { information } from "../../constants/information"
import { forUsers } from "../../constants/forUsers"
import { footerMarkets } from "../../constants/footerMarkets"
</script>


<template>
    <div class="container mx-auto" style="font-family: 'Inter'">
        <div class="foot py-[43px]">
            <div class="w-[280px] first">
                <nuxt-link to="/"><img src="BrandLogo.png" class="mb-[18px]" alt=""></nuxt-link>
                <h1
                    class="text-[#505050] xl:w-[100%] md:w-[70%] sm:text-[16px] text-[10px] w-[60%] sm:w-[60%] lg:w-[80%] mb-[18px]">
                    Best information about the
                    company gies here but now lorem ipsum is</h1>
                <div class="flex gap-[12px]">
                    <i
                        class="rounded-full p-[6px] bg-[#BDC4CD] text-[18px] text-white duration-300 hover:cursor-pointer hover:bg-[#3b5998] bx bxl-facebook"></i>
                    <i
                        class="rounded-full p-[6px] bg-[#BDC4CD] text-[18px] text-white duration-300 hover:cursor-pointer hover:bg-[#00acee] bx bxl-twitter"></i>
                    <i
                        class="rounded-full p-[6px] bg-[#BDC4CD] text-[18px] text-white duration-300 hover:cursor-pointer hover:bg-[#0072b1] bx bxl-linkedin"></i>
                    <i
                        class="rounded-full p-[6px] bg-[#BDC4CD] text-[18px] text-white duration-300 hover:cursor-pointer hover:bg-[#E4405F] bx bxl-instagram"></i>
                    <i
                        class="rounded-full p-[6px] bg-[#BDC4CD] text-[18px] text-white duration-300 hover:cursor-pointer hover:bg-[#c4302b] bx bxl-youtube"></i>
                </div>
            </div>
            <div class="first">
                <h1 class="font-medium mb-[10px] md:text-[16px] text-[13px]">About</h1>
                <h1 v-for="el in about"
                    class="text-[#8B96A5] md:text-[16px] text-[12px] hover:text-black hover:cursor-pointer duration-300"
                    :class="el === 'Blogs' ? '' : 'mb-10px'">{{ el }}</h1>
            </div>
            <div class="first">
                <h1 class="font-medium mb-[10px] md:text-[16px] text-[13px]">Partnership</h1>
                <h1 v-for="el in about"
                    class="text-[#8B96A5] md:text-[16px] text-[12px] hover:text-black hover:cursor-pointer duration-300"
                    :class="el === 'Blogs' ? '' : 'mb-10px'">{{ el }}</h1>
            </div>
            <div class="first">
                <h1 class="font-medium mb-[10px] md:text-[16px] text-[13px]">Information</h1>
                <h1 v-for="el in information"
                    class="text-[#8B96A5] md:text-[16px] text-[12px] hover:text-black hover:cursor-pointer duration-300"
                    :class="el === 'Blogs' ? '' : 'mb-10px'">{{ el }}</h1>
            </div>
            <div class="first">
                <h1 class="font-medium mb-[10px] md:text-[16px] text-[13px]">For Users</h1>
                <h1 v-for="el in forUsers"
                    class="text-[#8B96A5] md:text-[16px] text-[12px] hover:text-black hover:cursor-pointer duration-300"
                    :class="el === 'Blogs' ? '' : 'mb-10px'">{{ el }}</h1>
            </div>
            <div>
                <h1 class="font-medium mb-[10px] md:text-[16px] text-[13px]">Get App</h1>
                <img v-for="el in footerMarkets" class="mb-[10px]" :src="el" alt="">
            </div>
        </div>
    </div>
    <div class="bg-[#EFF2F4]" style="font-family: 'Inter'">
        <div class="container bottom mx-auto flex justify-between items-center py-[23px] text-[#606060]">
            <h1>© {{ new Date().getFullYear() }} Ecommerce.</h1>
            <select name="languages" class="border-none bg-[#EFF2F4] outline-none" id="">
                <option class="bg-white" v-for="el in footerLanguages" :value="el.title">{{ el.title }}</option>
            </select>
        </div>
    </div>
</template>


<style lang="scss" scoped>
@media only screen and (min-width: 600px) {
    .foot {
        display: grid;
        grid-template-columns: 30% 14% 14% 14% 14% 14%;
    }

}

@media screen and (max-width: 600px) {
    .first {
        margin-bottom: 50px;
        font-size: 16px;
    }

    .foot{
        padding-left: 20px;
    }
    
    .bottom{
        padding: 20px 40px;
    }
}
</style>