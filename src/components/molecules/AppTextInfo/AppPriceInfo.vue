<script setup>
import AppContainer from "@/components/atoms/AppContainer/AppContainer.vue"

const props = defineProps({
  count: {
    type: String,
    default: "$3,297,09",
  },
  countText: {
    type: String,
    default: "02 tasks",
  },
})
</script>

<template>
  <AppContainer class="flex flex-col items-start justify-start w-max gap-[5px]">
    <h1
      class="text-black font-bold xl:text-[20px] desktop:text-[30px] max-h-max w-max !p-0 !m-0 leading-none"
    >
      {{ props.count }}
    </h1>
    <p class="relative text-gray-400 xl:text-[14px] desktop:text-[20px]">{{ props.countText }}</p>
  </AppContainer>
</template>
