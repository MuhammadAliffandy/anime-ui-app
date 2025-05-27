<script setup>
import AppContainer from "@/components/atoms/AppContainer/AppContainer.vue"

const props = defineProps({
  text: {
    type: String,
    default: "",
  },
  class: {
    type: String,
    default: "",
  },
  isSelect: {
    type: Boolean,
    default: false,
  },
})
</script>

<template>
  <AppContainer
    :class="`flex items-center justify-start gap-[10px] xl:text-[9px] desktop:text-[14px]  px-[10px] py-[4px] rounded-full border-2 ${props.class} border-black ${props.isSelect ? 'bg-black' : ' '}`"
  >
    <AppContainer
      v-if="props.isSelect"
      class="w-[5px] h-[5px] rounded-full bg-white"
    ></AppContainer>
    <p :class="props.isSelect ? 'text-white' : 'text-black'">{{ props.text }}</p>
  </AppContainer>
</template>
