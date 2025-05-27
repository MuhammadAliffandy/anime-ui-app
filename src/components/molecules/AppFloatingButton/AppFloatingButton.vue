<script setup>
import { ref } from "vue"
import AppContainer from "@/components/atoms/AppContainer/AppContainer.vue"
import AppButton from "@/components/atoms/AppButton/AppButton.vue"
import { Icon } from "@iconify/vue"

const isOpen = ref(true)

const iconDummy = [
  { icon: "lets-icons:bookmark-light" },
  { icon: "solar:settings-minimalistic-outline" },
  { icon: "circum:calendar" },
  { icon: "solar:home-2-bold" },
]
</script>

<template>
  <AppContainer class="bottom-6 right-6 z-50 flex flex-col items-center gap-3">
    <!-- Icon buttons shown when open -->
    <transition-group name="slide-up" tag="div" class="flex flex-col-reverse items-center gap-3">
      <template v-if="isOpen">
        <AppButton
          v-for="(item, index) in iconDummy"
          :key="item.icon"
          :class="`bg-white rounded-full p-4 border-2 border-black animate__animated animate__bounceInUp animate__delay-${index}s `"
        >
          <Icon :icon="item.icon" width="30" class="text-black" />
        </AppButton>
      </template>
    </transition-group>

    <!-- FAB Toggle -->
    <AppButton
      @click="isOpen = !isOpen"
      class="bg-black text-white rounded-full p-5 shadow-lg transition-transform duration-300 hover:scale-110"
    >
      <Icon :icon="isOpen ? 'solar:close-circle-bold' : 'lineicons:menu-meatballs-1'" width="30" />
    </AppButton>
  </AppContainer>
</template>

<style scoped>
.slide-up-enter-from,
.slide-up-leave-to {
  opacity: 0;
  transform: translateY(20px);
}
.slide-up-enter-active,
.slide-up-leave-active {
  transition: all 0.3s ease;
}
</style>
