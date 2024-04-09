<template>
  <div
    class="bg-gradient-to-r from-[#54BE96] via-[#FFFFFF] via-70% to-[#54BE96] w-[100%] max-w-[90rem] py-10 px-10"
  >
    <div class="md:flex justify-center items-center">
      <div class="animate-slide-left">
        <h1 class="font-bold lg:text-[80px] text-[40px] max-w-[600px]  mb-[2rem] text-[#191A15]">
          We’re here to Increase your Productivity
        </h1>
        <img src="@/assets/Vector1.svg" alt="vector" class="mb-[4rem]" />
        <p class="font-medium text-[18px] text-[#000000]  max-w-[600px] mb-[3rem]">
          Let's make your work more organize and easily using the Taskio
          Dashboard with many of the latest featuresin managing work every day.
        </p>
        
        <div class="flex">
          <Button class="text-[18px] font-medium rounded-full py-2.5 px-4 mb-[3rem]"> Try free trial </Button>
          <span class="text-2xl  ml-[2rem] flex">
            <i class="bi bi-play-circle"></i>
            <p class="text-[#191A15] font-medium text-[18px] ml-3">View Demo</p>
          </span>
        </div>
      </div>

      <div class="animate-slide-right">
        <img src="@/assets/Group1.svg" alt="group1" class="text-xl">
      </div>
    </div>
  </div>
</template>

<script setup>
import Button from "@/components/ButTon"
</script>

<style>
@keyframes slideInLeft {
  0% {
    transform: translateX(-100%);
  }
  100% {
    transform: translateX(0);
  }
}

@keyframes slideInRight {
  0% {
    transform: translateX(100%);
  }
  100% {
    transform: translateX(0);
  }
}

.animate-slide-left {
  animation: slideInLeft 1s ease-in-out;
}

.animate-slide-right {
  animation: slideInRight 1s ease-in-out;
}
</style>
