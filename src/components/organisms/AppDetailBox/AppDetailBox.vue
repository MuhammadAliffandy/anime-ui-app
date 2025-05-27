<script setup>
import AppContainer from "@/components/atoms/AppContainer/AppContainer.vue"
import AppTagList from "@/components/molecules/AppTagList/AppTagList.vue"
import AppTextChip from "@/components/molecules/AppTextChip/AppTextChip.vue"
import AppTag from "@/components/molecules/AppTag/AppTag.vue"
import { Icon } from "@iconify/vue"

const dataDummy = [
  {
    text: "Morning text",
    isSelect: true,
  },
  { text: "Clear Feedback", isSelect: true },
  { text: "Complete At least 19:00 PM", isSelect: false },
  { text: "Setup Computer", isSelect: false },
]
</script>

<template>
  <!-- 
  preserveAspectRatio="none"
  class="w-full h-full" 
  -->
  <AppContainer class="h-full w-[30%] relative animate__animated animate__zoomIn animate__delay-1s">
    <svg
      preserveAspectRatio="none"
      class="relative w-full h-full"
      viewBox="0 0 948 1233"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <foreignObject x="-65.6" y="-65.6" width="1079.2" height="1364.2"
        ><div
          xmlns="http://www.w3.org/1999/xhtml"
          style="
            backdrop-filter: blur(10.8px);
            clip-path: url(#bgblur_0_35_6_clip_path);
            height: 100%;
            width: 100%;
          "
        ></div
      ></foreignObject>
      <path
        data-figma-bg-blur-radius="65.6"
        d="M948 902C948 935.137 921.137 962 888 962H414C364.294 962 324 1002.29 324 1052V1173C324 1206.14 297.137 1233 264 1233H60C26.8629 1233 0 1206.14 0 1173V60C0 26.863 26.8629 0 60 0H888C921.137 0 948 26.8629 948 60V902Z"
        fill="#D9D9D9"
        fill-opacity="0.42"
      />
      <defs>
        <clipPath id="bgblur_0_35_6_clip_path" transform="translate(65.6 65.6)">
          <path
            d="M948 902C948 935.137 921.137 962 888 962H414C364.294 962 324 1002.29 324 1052V1173C324 1206.14 297.137 1233 264 1233H60C26.8629 1233 0 1206.14 0 1173V60C0 26.863 26.8629 0 60 0H888C921.137 0 948 26.8629 948 60V902Z"
          />
        </clipPath>
      </defs>
    </svg>
    <AppContainer
      class="absolute z-1 w-full h-full flex flex-col items-start justify-start p-[40px] top-0 gap-[20px]"
    >
      <AppContainer>
        <p class="text-black font-bold">Today, Dec 10, 2025</p>
        <AppTextChip textClass="text-white" />
      </AppContainer>
      <AppTagList :tags="dataDummy" />
      <AppContainer class="flex flex-col absolute bottom-2 left-2">
        <AppButton
          class="bg-gray-200 xl:text-[12px] px-[20px] py-[10px] rounded-full text-black flex items-center justify-items-center max-w-max"
        >
          Light Mode
        </AppButton>
        <AppContainer class="flex items-stretch">
          <AppButton
            class="bg-transparent rounded-full p-[10px] py-[28px] border-[2px] border-black"
          >
            <Icon icon="bi:sun-fill" class="text-white xl:text-[18px] text-[30px]" />
          </AppButton>
          <AppButton class="bg-black rounded-full p-[10px] py-[24px] border-[2px] border-black">
            <Icon icon="ri:moon-fill" class="text-white xl:text-[18px] text-[30px]" />
          </AppButton>
        </AppContainer>
      </AppContainer>
    </AppContainer>
  </AppContainer>
</template>
