<script setup>
import AppHeaderTool from "@/components/organisms/AppHeaderTool/AppHeaderTool.vue"
import AppContainer from "@/components/atoms/AppContainer/AppContainer.vue"
import AppDetailBox from "@/components/organisms/AppDetailBox/AppDetailBox.vue"
import AppPerformanceBox from "@/components/organisms/AppPerformanceBox/AppPerformanceBox.vue"
import AppWalletInfo from "@/components/organisms/AppWalletInfo/AppWalletInfo.vue"
import AppDailyInfo from "@/components/organisms/AppDailyInfo/AppDailyInfo.vue"
import AppTextChip from "@/components/molecules/AppTextChip/AppTextChip.vue"
import AppChip from "@/components/atoms/AppChip/AppChip.vue"
import AppFloatingButton from "@/components/molecules/AppFloatingButton/AppFloatingButton.vue"
</script>

<template>
  <main
    id="home-view"
    class="flex items-center justify-center bg-white h-screen w-full bg-[url('/image/bee.svg')] bg-[length:150%_300%] bg-center bg-white/30 relative"
  >
    <AppContainer
      class="relative w-full h-full backdrop-blur-md bg-center bg-no-repeat bg-[length:55%] bg-[url('/image/bee.svg')] shadow-xl p-6 flex flex-col items-stretch overflow-hidden"
    >
      <AppHeaderTool />
      <AppContainer class="px-[30px] h-full w-full flex items-stretch justify-start">
        <AppContainer class="w-[8%] py-[30px] h-full flex items-end justify-center">
          <AppFloatingButton />
        </AppContainer>
        <AppContainer class="w-full h-full flex-col flex p-[20px]">
          <!--  -->
          <AppContainer class="w-full h-[100%] flex items-stretch">
            <AppContainer class="flex flex-col justify-between items-start h-full w-[100%]">
              <AppContainer class="flex flex-col relative">
                <p
                  class="text-white text-[42px] animate__animated animate__fadeInLeft animate__delay-5s"
                >
                  Today
                </p>
                <AppChip
                  :text="'a best'"
                  class="text-[32px] relative left-[20px] bottom-[10px] animate__animated animate__fadeInLeft animate__delay-5s"
                />
                <AppChip
                  :text="'day to win'"
                  class="text-[32px] relative left-[40px] bottom-[10px] animate__animated animate__fadeInLeft animate__delay-5s"
                />
              </AppContainer>
              <AppTextChip
                class="text-black animate__animated animate__fadeInLeft animate__delay-5s"
                :text="'Daily'"
                :textChip="'Summary'"
              />
            </AppContainer>
            <AppDetailBox />
          </AppContainer>
          <!--  -->
          <AppContainer class="w-full h-[50%] flex items-stretch gap-[20px] relative">
            <AppContainer class="w-[25%] h-full p-[10px]">
              <AppDailyInfo class="animate__animated animate__zoomIn animate__delay-4s" />
            </AppContainer>
            <AppContainer class="w-[25%] h-full p-[10px]">
              <AppDailyInfo class="animate__animated animate__zoomIn animate__delay-4s" />
            </AppContainer>
            <AppContainer class="w-[35%] h-full p-[10px]">
              <AppWalletInfo />
            </AppContainer>
            <AppContainer class="w-[15%] h-full flex items-stretch relative">
              <AppContainer class="absolute z-1 w-full h-[135%] bottom-0 p-[10px]">
                <AppPerformanceBox />
              </AppContainer>
            </AppContainer>
          </AppContainer>
        </AppContainer>
      </AppContainer>
    </AppContainer>

    <!--  -->
    <AppContainer
      class="absolute bg-black top-0 w-full h-full flex sm:flex md:flex lg:flex xl:hidden desktop:hidden items-center justify-center"
    >
      <p class="text-yellow-600 p-[20px] border-2 border-yellow-600 w-max">Only Deskstop Mode</p>
    </AppContainer>
  </main>
</template>
