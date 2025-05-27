<script setup>
import AppContainer from "@/components/atoms/AppContainer/AppContainer.vue"
import AppChip from "@/components/atoms/AppChip/AppChip.vue"

const props = defineProps({
  text: {
    type: String,
    default: "Habit",
  },
  textChip: {
    type: String,
    default: "tracker",
  },
  textClass: {
    type: String,
    default: "",
  },
})
</script>

<template>
  <AppContainer class="flex items-center">
    <p :class="`font-bold text-[35px] ${props.textClass} `">{{ props.text }}</p>
    <AppChip class="text-[24px]" :text="props.textChip" />
  </AppContainer>
</template>
