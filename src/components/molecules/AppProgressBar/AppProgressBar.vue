<script setup>
import AppContainer from "@/components/atoms/AppContainer/AppContainer.vue"

const props = defineProps({
  start: {
    type: Number,
    default: 0,
  },
  end: {
    type: Number,
    default: 100,
  },
  indicator: {
    type: Number,
    default: 50,
  },
})
</script>

<template>
  <AppContainer class="flex flex-col">
    <AppContainer
      class="flex items-center justify-between w-full text-gray-500 xl:text-[10px] desktop:text-[12px] px-[10px]"
    >
      <p>{{ props.start }}</p>
      <p>{{ props.end / 2 }}</p>
      <p>{{ props.end }}</p>
    </AppContainer>
    <AppContainer class="flex p-[5px] bg-black w-full rounded-full">
      <AppContainer
        :class="`bg-white desktop:h-[12px] xl:h-[6px]  rounded-full w-[${props.indicator ? (props.end / 100) * props.indicator : '60'}%] `"
      ></AppContainer>
    </AppContainer>
  </AppContainer>
</template>
