<script setup>
const props = defineProps({
    class: {
        type: String,
        default: 'flex flex-col',
    }
})
</script>

<template>
    <div :class="props.class">
        <slot></slot>
    </div>
</template>

