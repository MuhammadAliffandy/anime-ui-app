<script setup>
import AppContainer from "@/components/atoms/AppContainer/AppContainer.vue"
import AppTextField from "@/components/atoms/AppTextField/AppTextField.vue"
import AppButton from "@/components/atoms/AppButton/AppButton.vue"
import { Icon } from "@iconify/vue"

const emit = defineEmits(["click", "input"])
</script>
<template>
  <AppContainer class="flex flex-row items-center relative">
    <AppButton class="bg-black rounded-full p-[16px] z-[1] absolute">
      <Icon icon="ri:search-line" class="text-white text-[35px]" @click="emit('click')" />
    </AppButton>
    <AppTextField
      class="left-[30px] pl-[40px] bg-white text-black py-[20px] pr-[20px] rounded-full relative h-full w-full animate__animated animate__fadeInLeft"
      @input="emit('input')"
    />
  </AppContainer>
</template>
