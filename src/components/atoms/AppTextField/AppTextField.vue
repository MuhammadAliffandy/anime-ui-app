<script setup>
const emit = defineEmits(["input"])

const props = defineProps({
  id: {
    type: String,
    default: "text",
  },
  type: {
    type: String,
    default: "text",
  },
  placeholder: {
    type: String,
    default: "Type here...",
  },
  class: {
    type: String,
    default: "text-black border-2 px-[15px] py-[8px] rounded-3xl w-full",
  },
})
</script>

<template>
  <input
    :class="props.class"
    :type="props.type"
    :placeholder="props.placeholder"
    @input="emit(input)"
  />
</template>

<style scoped></style>
