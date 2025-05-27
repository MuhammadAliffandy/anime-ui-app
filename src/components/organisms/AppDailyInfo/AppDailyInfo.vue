<script setup>
import AppContainer from "@/components/atoms/AppContainer/AppContainer.vue"
import AppTextInfo from "@/components/molecules/AppTextInfo/AppTextInfo.vue"
import { Icon } from "@iconify/vue"

const props = defineProps({
  class: {
    type: String,
    default: "",
  },
})
</script>

<template>
  <AppContainer :class="`w-full h-full relative ${props.class} `">
    <svg
      preserveAspectRatio="none"
      class="w-full h-full absolute"
      viewBox="0 0 677 410"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="M473 55C473 137.843 540.157 205 623 205V205C652.823 205 677 229.177 677 259V320C677 369.706 636.706 410 587 410H90C40.2944 410 0 369.706 0 320V90C0 40.2944 40.2944 0 90 0H418C448.376 0 473 24.6243 473 55V55Z"
        fill="white"
      />
    </svg>
    <AppContainer class="w-full h-full p-[25px] xl:p-[20px] flex flex-col justify-between absolute">
      <h1 class="text-black font-bold xl:text-[20px] text-[24px]">Todo</h1>
      <AppContainer class="w-full flex items-center justify-center">
        <AppTextInfo />
      </AppContainer>
      <AppButton
        class="bg-black hover:bg-white rounded-full xl:p-[15px] p-[22px] shadow-xl w-max h-max absolute z-10 top-0 xl:right-2 right-0 animate__animated animate__fadeInTopRight animate__delay-5s"
      >
        <Icon
          icon="eva:diagonal-arrow-right-up-fill"
          class="text-white hover:text-black xl:text-[30px] text-[40px]"
        />
      </AppButton>
    </AppContainer>
  </AppContainer>
</template>
