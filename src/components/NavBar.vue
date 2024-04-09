<template>
    <div class="bg-gradient-to-r from-[#52BDAA] via-[#FFFFFF] via-70% to-[#52BDAA] py-2 px-10 md:flex items-center justify-around ">
        <div class="md:mx-2">
            <h1 class="text-[#54BD95]  font-semibold text-[50px] cursor-pointer">Biccas</h1>
        </div>

        <span @click="MenuOpen(b)" class="absolute md:hidden right-6 top-1.5 cursor-pointer text-white text-6xl">
            <i :class="[open ? 'bi bi-x' : 'bi bi-filter-left']"></i>
        </span>

        <ul class="md:flex md:items-center md:px-0 px-12 md:pb-0 pb-10 md:static absolute md:shadow-none shadow  md:w-auto w-full top-25 duration-700 ease-in"
        :class="[open ? 'left-0' : 'left-[-100%]']"
        >
            <li class="md:mx-8 md:my-0 my-6" v-for="link in Links" :key="link.name">
                <a :href="link.link" class="text-[#000000]  text-[18px] font-medium " :class="{'text-[#A6A6A6] text-[16px]': link.name === 'Product' || link.name === 'FAQ' || link.name === 'Blog' || link.name === 'About Us'}">{{link.name}}</a>
            </li>

            <div class="md:mx-8 md:my-0 my-6 inline-block md:hidden lg:inline-block">
                <a class=" text-[#A6A6A6] text-[16px] font-medium cursor cursor-pointer">Login</a>
            </div>

            <Button class="inline-block md:hidden lg:inline-block">
                Sign Up
            </Button>
        </ul>
    </div>
</template>

<script>
import Button from "@/components/ButTon"
import {ref} from 'vue'
export default {
    components: {
   Button
  },
   setup(){
    let open = ref(false)
    let Links = [
        {name : "Home", link : "#"},
        {name : "Product", link : "#"},
        {name : "FAQ", link : "#"},
        {name : "Blog", link : "#"},
        {name : "About Us", link : "#"},
    ]

    function MenuOpen (){
        open.value = !open.value
    }
    return{Links, open, MenuOpen}
    }
   }
</script>
 
<style>
