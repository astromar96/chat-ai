<template>
    <button :disabled='disabled' :class="{
        'button': true,
        'button--primary': type === 'primary',
        'button--secondary': type === 'secondary',
        'button--link': type === 'link',
        'button--full-width': fullWidth,
        'button--left-aligned-content': leftAlignedContent,
    }">
        <template v-if="!text">
            <slot />
        </template>
        <template v-else>
            <span>{{ text }}</span>
        </template>
    </button>
</template>

<script setup>
defineProps({
    text: String,
    disabled: Boolean,
    fullWidth: Boolean,
    leftAlignedContent: Boolean,
    type: {
        type: String,
        default: 'primary',
        validator: (value) => ['primary', 'secondary', 'link'].includes(value),
    },
})
</script>

<style></style>