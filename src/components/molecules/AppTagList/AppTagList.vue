<script setup>
import AppTag from "@/components/molecules/AppTag/AppTag.vue"
import AppContainer from "@/components/atoms/AppContainer/AppContainer.vue"

const props = defineProps({
  tags: {
    type: Array,
    default: () => [],
  },
})
</script>

<template>
  <AppContainer class="flex flex-wrap w-full">
    <template v-for="(item, index) in tags" :key="item.text">
      <AppTag
        :text="item.text"
        :isSelect="item.isSelect"
        :class="`animate__animated animate__bounceInRight animate__delay-${index + 2}s`"
      />
    </template>
  </AppContainer>
</template>
