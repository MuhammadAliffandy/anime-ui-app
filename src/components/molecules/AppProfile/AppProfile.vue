<script setup>
import AppContainer from "@/components/atoms/AppContainer/AppContainer.vue"
import AppImage from "@/components/atoms/AppImage/AppImage.vue"

const props = defineProps({
  textProfile: {
    type: String,
    default: "Funday",
  },
  class: {
    type: String,
    default: "",
  },
})
</script>

<template>
  <AppContainer
    :class="`w-max h-full flex flex-row py-[6px] px-[12px] bg-white items-center gap-[10px] rounded-full ${props.class}`"
  >
    <p class="text-[18px] xl:text-[16px] text-black font-bold">{{ props.textProfile }}</p>
    <AppImage class="w-[60px] h-[60px] xl:w-[50px] xl:h-[50px] rounded-full" />
  </AppContainer>
</template>
