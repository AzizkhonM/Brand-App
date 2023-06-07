<script setup>

import { main1 } from "../constants/main1"
import { offers } from "../constants/offers"
import { home } from "../constants/home";
import { gadgets } from "../constants/gadgets"
import { units } from "../constants/units"
import { recommendations } from "../constants/recommendations";
import { suppliers } from "../constants/suppliers"
import { services } from "../constants/services"

const days = ref(4)
const hours = ref(13)
const minutes = ref(59)
const seconds = ref(5)

setInterval(() => {
    if (seconds.value === 0) {
        seconds.value = 59
        minutes.value -= 1
    } else {
        seconds.value -= 1
    }
}, 1000);

</script>


<template>
    <Header />
    <div class="bg-[#F7FAFC] py-[20px]" style="font-family: 'Inter'">
        <div class="container mx-auto">
            <div class="top mb-[30px] rounded-[6px] border-[1px] bg-white py-[19px] px-[13px]">
                <div class="w-[300px] mr-[13px]">
                    <div v-for="el in main1"
                        class="categ py-[11px] px-[10px] rounded-[6px] text-[#505050] hover:cursor-pointer hover:bg-[#E5F1FF] hover:text-black duration-300">
                        <h1>{{ el.title }}</h1>
                    </div>
                </div>
                <div class="banner mr-[20px] w-[825px] pt-[53px] pl-[43px]">
                    <h1 class="text-[#1C1C1C] latest text-[28px]">Latest Trending</h1>
                    <h1 class="text-[#1C1C1C] electronic text-[32px] font-bold mb-[17px]">Electronic items</h1>
                    <nuxt-link to="/mobile"><button
                        class="font-medium text-[#1C1C1C] py-[10px] px-[16px] rounded-[6px] bg-white hover:shadow-lg duration-300">Learn
                        more</button></nuxt-link>
                </div>
                <div class="w-auto gap-[17px] items-center hi">
                    <div class="rounded-[6px] p-[10px] bg-[#E3F0FF] w-[100%]">
                        <div class="flex gap-[20px] mb-[25px] justify-start items-center">
                            <img src="/Avatar.png" width="60" alt="">
                            <h1 class="tracking-[1px] text-[22px] w-[140px]">Hi, user let’s get stated</h1>
                        </div>
                        <div class="mb-[7px]">
                            <button
                                class="py-[10px] rounded-[6px] text-white w-full bg-[#127FFF] hover:bg-[#0045ab] duration-300 ">Join
                                now</button>
                        </div>
                        <div>
                            <button
                                class="border-[1px] w-full text-[#0D6EFD] rounded-[6px] py-[10px] bg-white hover:bg-[#f4f4f4] duration-300">Login</button>
                        </div>
                    </div>
                    <div class="coupons">
                        <div
                        class="flex items-center mb-[15px] p-[20px] bg-[#F38332] text-[20px] text-white tracking-[1px] rounded-[6px]">
                        <h1 class="">Get US $10 off with a new supplier</h1>
                    </div>
                    <div
                        class="flex items-center p-[20px] bg-[#55BDC3] text-[20px] text-white tracking-[1px] rounded-[6px]">
                        <h1 class="">Send quotes with supplier preferences</h1>
                    </div>
                    </div>
                </div>
            </div>
            <div class="lg:flex mb-[30px] rounded-[6px] border-[1px] bg-white" style="">
                <div class="lg:w-[375px] dealsn lg:gap-0 gap-4 items-center w-full flex lg:inline justify-center p-[22px]">
                    <h1 class="text-[20px] worddeals font-semibold">Deals and offers</h1>
                    <h1 class="text-[16px] hygiene text-[#8B96A5] lg:mb-[21px]">Hygiene equipments</h1>
                    <div class="flex gap-[10px] timer">
                        <div
                            class="w-[50px] h-[55px] text-white bg-[#606060] rounded-[6px] grid grid-cols-1 items-center justify-center place-content-center">
                            <h1 class="text-center font-bold">{{ days.toString().padStart(2, "0") }}</h1>
                            <h1 class="text-center text-[12px]">Days</h1>
                        </div>
                        <div
                            class="w-[50px] h-[55px] text-white bg-[#606060] rounded-[6px] grid grid-cols-1 items-center justify-center place-content-center">
                            <h1 class="text-center font-bold">{{ hours.toString().padStart(2, "0") }}</h1>
                            <h1 class="text-center text-[12px]">Hour</h1>
                        </div>
                        <div
                            class="w-[50px] h-[55px] text-white bg-[#606060] rounded-[6px] grid grid-cols-1 items-center justify-center place-content-center">
                            <h1 class="text-center font-bold">{{ minutes.toString().padStart(2, "0") }}</h1>
                            <h1 class="text-center text-[12px]">Min</h1>
                        </div>
                        <div
                            class="w-[50px] h-[55px] text-white bg-[#606060] rounded-[6px] grid grid-cols-1 items-center justify-center place-content-center">
                            <h1 class="text-center font-bold">{{ seconds.toString().padStart(2, "0") }}</h1>
                            <h1 class="text-center text-[12px]">Sec</h1>
                        </div>
                    </div>
                </div>
                <div class="w-full offers">
                    
                    <div  v-for="el in offers">
                        <Deals :offer="el" />    
                    </div>
                </div>
            </div>
            <div class="md:flex mb-[30px] rounded-[6px] border-[1px] bg-white homebig">
                <div class="home md:w-[375px] w-full h-[310px] pt-[25px] pl-[23px]">
                    <h1 class="text-[#1C1C1C] font-semibold text-[22px] w-[130px] mb-[22px]">Home and Outdors</h1>
                    <button class="bg-white px-[20px] py-[13px] rounded-[6px] hover:shadow-lg duration-300">Source now</button>
                </div>
                <div class="w-full homeprod">
                    <div v-for="card in home">
                        <Source :card="card" />
                    </div>
                </div>
            </div>
            <div class="md:flex mb-[30px] rounded-[6px] border-[1px] bg-white homebig">
                <div class="gadgets md:w-[375px] w-full h-[310px] pt-[25px] pl-[23px]">
                    <h1 class="text-[#1C1C1C] font-semibold text-[22px] w-[150px] mb-[22px]">Consumer electronics and gadgets</h1>
                    <button class="bg-white px-[20px] py-[13px] rounded-[6px] hover:shadow-lg duration-300">Source now</button>
                </div>
                <div class="w-full homeprod">
                    <div v-for="card in gadgets">
                        <Source :card="card" />
                    </div>
                </div>
            </div>
            <div class="requests w-full sm:justify-between h-auto sm:flex mb-[30px] rounded-[6px] border-[1px] border-[#52a3ff] py-[33px] px-[35px]">
                <div class="sm:mb-0 mb-[30px]">
                    <h1 class="text-white xl:w-[440px] md:w-[150px] sm:w-[100px] sm:text-[15px] md:text-[27px] lg:w-[300px] lg:text-[35px] font-bold  xl:text-[35px] mb-[13px]">An easy way to send requests to all suppliers</h1>
                    <h1 class="text-white xl:w-[440px] md:w-[150px] sm:w-[100px] sm:text-[10px] md:text-[14px] lg:w-[300px] lg:text-[14px] xl:text-[18px]">Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt.</h1>
                </div>
                <div class="xl:w-[520px] sm:w-[400px] md:w-[450px] lg:w-[500px] py-[25px] px-[23px] bg-white">
                    <h1 class="font-bold text-[22px] mb-[18px]">Send quote to suppliers</h1>
                    <input type="text" placeholder="What item you need?" class="w-full rounded-[6px] p-[13px] border-gray-300 mb-[18px]">
                    <textarea name="" id="" class="w-full p-[13px] border-gray-300 rounded-[6px] mb-[18px]" placeholder="Type more details" rows="3"></textarea>
                    <div class="mb-[18px]">
                        <input placeholder="Quantity" type="number" class="p-[13px] mr-[20px] w-[45%] rounded-[6px] border-gray-300">
                        <select class="p-[13px] rounded-[6px] border-gray-300" name="" id="">
                            <option v-for="el in units" :value="el">{{ el }}</option>
                        </select>
                    </div>
                    <button class="rounded-[6px] p-[12px] text-[18px] text-white bg-[#127FFF] hover:bg-[#0045ab] duration-300">Send inquiry</button>
                </div>
            </div>
            <h1 class="mb-[18px] font-bold text-[26px] recitem">Recommended items</h1>
            <div class="gap-[23px] mb-[18px] items">
                <div v-for="el in recommendations" class="recitemcard border-[1px] p-[20px] rounded-[6px] bg-white hover:cursor-pointer">
                    <div class="w-full flex justify-center mb-[17px]">
                        <img :src="'/' + el.img" width="250" alt="">
                    </div>
                    <h1 class="font-medium text-[18px]">${{ el.price }}</h1>
                    <h1 class="w-full text-[#8B96A5] text-[18px]">{{el.title}}</h1>
                </div>
            </div>
            <h1 class="mb-[18px] font-bold text-[26px] extser">Our extra services</h1>
            <div class="gap-[25px] mb-[18px] grid lg:grid-cols-4 sm:grid-cols-2 px-7">
                <div class="" v-for="service in services">
                    <Services :service="service" />
                </div>
            </div>
            <h1 class="mb-[18px] font-bold suppreg text-[26px]">Suppliers by region</h1>
            <div class="regions gap-[21px] mb-[18px]">
                <div v-for="i in suppliers" class="flex items-center">
                    <Suppliers :i="i" />
                </div>
            </div>
        </div>
    </div>

    <Email />
</template>


<style lang="scss" scoped>
.banner {
    background-image: url("../public/Banner.png");
    background-repeat: no-repeat;
    background-size: cover;
}

.home{
    background-image: url("../public/Home.png");
    background-size: cover;
    background-repeat: no-repeat;
}

.gadgets{
    background-image: url("../public/Gadgets.png");
    background-size: cover;
    background-repeat: no-repeat;
}



.requests{
    background-image: url("../public/Requests.png");
    background-size: cover;
    background-repeat: no-repeat;
}

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


@media screen and (min-width: 600px) {
    .regions{
        display: grid; grid-template-columns: 18.9% 18.9% 18.9% 18.9% 18.9%;
    }

    .homeprod{
        display: grid; grid-template-columns: 25% 25% 25% 25%;
    }

    .offers{
        display: grid; grid-template-columns: 20% 20% 20% 20% 20%;
    }

    .items{
        display: grid; grid-template-columns: 18.8% 18.8% 18.8% 18.8% 18.8%;
    }

    .home{
    background-image: url("../public/Home.png");
    background-size: cover;
    background-repeat: no-repeat;
}

.gadgets{
    background-image: url("../public/Gadgets.png");
    background-size: cover;
    background-repeat: no-repeat;
}

    .top{
        display: flex;
    }

    .hi{
        display: grid; grid-template-columns: 100%;
    }
}

@media screen and (max-width: 600px) {
    .regions{
        padding: 20px;
    }

    .suppreg{
        margin-left: 20px;
    }

    .extser{
        margin-left: 20px;
    }

    .recitem{
        margin-left: 20px;
    }

    .recitemcard{
        margin-left: 5px;
        margin-right: 5px;
    }

    .items{
        display: grid; grid-template-columns: 48% 48%;
        gap: 10px;
    }

    .homeprod{
        display: grid; grid-template-columns: 50% 50%;

    }

    .homebig{
        padding: 15px
    }

    .offers{
        display: grid; grid-template-columns: 49% 49%;
    }

    .top{
        display: grid;
        grid-template-columns: 50% 50%;
    }

    .banner{
        width: 100%;
    }

   
    .coupons{
        display: none;
    }

}

@media screen and (max-width: 500px) {
    .dealsn{
        display: inline;
        padding: 20px;
    }

    .worddeals{
        padding: 0px 0px 20px 20px;
    }

    .hygiene{
        padding: 0px 0px 20px 20px;
    }

    .timer{
        padding: 0 0 0 20px;
    }
}


@media screen and (max-width: 640px) {
    
    .latest{
        font-size: 20px;
    }

    .electronic{
        font-size: 23px;
    }

}

</style>