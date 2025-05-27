<script setup>

const props = defineProps({
    type : {
        type: String,
        default: 'button',
    },
    class: {
        type: String,
        default: '',
    }
})

</script>

<template>
    <button :type="props.button" :class="props.class" >
        <slot></slot>
    </button>
</template>

