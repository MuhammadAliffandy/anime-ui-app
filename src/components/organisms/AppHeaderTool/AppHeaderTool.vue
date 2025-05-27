<script setup>
import AppContainer from "@/components/atoms/AppContainer/AppContainer.vue"
import AppProfile from "@/components/molecules/AppProfile/AppProfile.vue"
import AppIconButton from "@/components/molecules/AppIconButton/AppIconButton.vue"
import AppButton from "@/components/atoms/AppButton/AppButton.vue"
import AppTextFieldButton from "@/components/molecules/AppTextFieldButton/AppTextFieldButton.vue"
import { Icon } from "@iconify/vue"
</script>

<template>
  <AppContainer class="w-full flex flex-row px-[60px] h-[10%] justify-between items-center">
    <AppTextFieldButton />
    <!--  -->
    <p class="text-black font-bold text-[24px] text-shadow-xl">ANI<br />ME</p>
    <!--  -->
    <AppContainer class="flex flex-row items-center gap-[15px] justify-stretch">
      <AppButton class="bg-white rounded-full p-[12px] animate__animated animate__zoomIn">
        <Icon icon="mingcute:notification-line" width="40" class="text-black" />
      </AppButton>
      <AppProfile class="animate__animated animate__zoomIn animate__delay-2s" />
      <AppIconButton class="animate__animated animate__zoomIn animate__delay-3s" />
    </AppContainer>
  </AppContainer>
</template>
