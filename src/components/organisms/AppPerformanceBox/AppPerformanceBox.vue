<script setup>
import AppContainer from "@/components/atoms/AppContainer/AppContainer.vue"
import AppProgressBar from "@/components/molecules/AppProgressBar/AppProgressBar.vue"
</script>

<template>
  <AppContainer
    class="w-full h-full flex flex-col justify-between rounded-[40px] bg-gray-200 gap-[15px] xl:p-[20px] p-[25px] animate__animated animate__zoomIn animate__delay-2s"
  >
    <h1 class="leading-none text-gray-500 xl:text-[12px] desktop:text-[20px]">Performance</h1>
    <AppProgressBar />
    <AppContainer class="flex flex-col h-[60%]">
      <h1 class="leading-none text-gray-500 desktop:text-[20px] xl:text-[12px]">Total Target</h1>
      <AppContainer class="flex flex-col relative">
        <h1 class="leading-none text-black font-bold xl:text-[40px] desktop:text-[75px]">35</h1>
        <h1
          class="leading-none text-black xl:text-[40px] desktop:text-[75px] top-[30%] left-[32%] rotate-45 absolute"
        >
          /
        </h1>
        <h1 class="leading-none text-black font-bold xl:text-[40px] desktop:text-[75px] self-end">
          80
        </h1>
      </AppContainer>
    </AppContainer>
  </AppContainer>
</template>
