<script setup>
const props = defineProps({
  text: {
    type: String,
    default: "AppChip",
  },
  class: {
    type: String,
    default: "",
  },
})
</script>

<template>
  <p
    :class="`max-w-max px-[14px] py-[2px] rounded-full text-black border-2 font-bold border-black ${props.class}`"
  >
    {{ text }}
  </p>
</template>
