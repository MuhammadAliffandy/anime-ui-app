<script setup>
import AppContainer from "@/components/atoms/AppContainer/AppContainer.vue"

const props = defineProps({
  count: {
    type: String,
    default: "82",
  },
  countText: {
    type: String,
    default: "Tasks",
  },
})
</script>

<template>
  <AppContainer class="flex w-max gap-[5px]">
    <h1
      class="text-black font-bold text-[4rem] xl:text-[3rem] max-h-max w-max !p-0 !m-0 leading-none"
    >
      {{ props.count }}
    </h1>
    <p class="relative text-gray-400 text-[1rem] xl:text-[1rem]">{{ props.countText }}</p>
  </AppContainer>
</template>
