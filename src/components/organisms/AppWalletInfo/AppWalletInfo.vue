<script setup>
import AppContainer from "@/components/atoms/AppContainer/AppContainer.vue"
import AppTextInfo from "@/components/molecules/AppTextInfo/AppTextInfo.vue"
import AppButton from "@/components/atoms/AppButton/AppButton.vue"
import AppPriceInfo from "@/components/molecules/AppTextInfo/AppPriceInfo.vue"
import { Icon } from "@iconify/vue"
</script>

<template>
  <AppContainer
    class="w-full h-full flex backdrop-blur-md bg-gray-400/40 rounded-[40px] gap-[20px] p-[10px] animate__animated animate__zoomIn animate__delay-3s"
  >
    <AppContainer class="w-[50%]">
      <AppContainer class="w-full xl:h-[40%] desktop:h-[50%]">
        <h1
          class="desktop:text-[24px] text-black font-bold xl:text-[18px] xl:py-[2px] desktop:py-[15px]"
        >
          Complete
        </h1>
      </AppContainer>
      <AppContainer class="w-full xl:h-[60%] desktop:h-[50%] relative">
        <svg
          preserveAspectRatio="none"
          class="w-full h-full absolute"
          viewBox="0 0 597 322"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M0 262C0 295.137 26.8629 322 60 322H341.414C358.81 322 375.35 314.45 386.747 301.306L586.529 70.895C593.282 63.1062 597 53.1431 597 42.8342V42.8342C597 19.1775 577.822 0 554.166 0H60C26.8629 0 0 26.8629 0 60V262Z"
            fill="white"
          />
        </svg>
        <AppContainer class="flex h-full w-full xl:p-[12px] desktop:p-[25px] absolute">
          <AppTextInfo />
          <AppButton
            class="bg-gray-400 rounded-full p-[2px] w-max h-max absolute z-10 xl:top-0 xl:right-0 desktop:top-1 desktop:right-1"
          >
            <Icon icon="eva:diagonal-arrow-right-up-fill" width="20" class="text-black" />
          </AppButton>
        </AppContainer>
      </AppContainer>
    </AppContainer>
    <AppContainer class="w-[50%] relative">
      <svg
        preserveAspectRatio="none"
        class="w-full h-full absolute"
        viewBox="0 0 531 505"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M531 445C531 478.137 504.137 505 471 505H220.161C203.866 505 188.271 498.372 176.963 486.64L16.802 320.489C6.02286 309.307 0 294.38 0 278.849V60C0 26.8629 26.8629 0 60 0H471C504.137 0 531 26.8629 531 60V445Z"
          fill="white"
        />
      </svg>
      <!--  -->
      <AppContainer
        class="absolute desktop:pt-[15px] xl:pt-[8px] desktop:pl-[25px] xl:pl-[10px] w-full h-full flex flex-col items-center justify-between"
      >
        <AppContainer class="flex gap-[10px] items-center">
          <Icon icon="solar:wallet-linear" class="text-black xl:text-[20px] desktop:text-[30px]" />
          <h1
            class="desktop:text-[22px] xl:text-[14px] text-black font-bold xl:py-[8px] desktop:py-[15px]"
          >
            Earnings
          </h1>
        </AppContainer>
        <AppContainer class="flex flex-col items-center justify-center w-full">
          <AppPriceInfo />
          <AppButton
            class="bg-gray-400 rounded-full p-[2px] w-max h-max self-end relative xl:bottom-4 desktop:bottom-2 right-2"
          >
            <Icon icon="eva:diagonal-arrow-right-up-fill" width="30" class="text-black" />
          </AppButton>
        </AppContainer>
      </AppContainer>
    </AppContainer>
  </AppContainer>
</template>
