<script setup>
import AppButton from "@/components/atoms/AppButton/AppButton.vue"
import { Icon } from "@iconify/vue"

const emit = defineEmits(["click"])

const props = defineProps({
  text: {
    type: String,
    default: "Category",
  },
  class: {
    type: String,
    default: "",
  },
})
</script>

<template>
  <AppButton
    :class="`bg-black p-[15px] rounded-[100px] flex flex-row gap-[10px] items-center ${props.class}`"
    @click="emit('click')"
    :type="'button'"
  >
    <Icon icon="ep:menu" class="text-white xl:text-[32px] text-[40px]" />
    <p class="text-[18px] xl:text-[16px] text-white font-bold">{{ props.text }}</p>
  </AppButton>
</template>
