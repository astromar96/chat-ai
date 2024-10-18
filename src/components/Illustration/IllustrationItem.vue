<template>
    <div :class="['intro__illustration', `intro__illustration--${customClass}`]">
        <div class='intro__illustration__image'>
            <slot name="image"></slot>
        </div>
        <div class="intro__illustration__title">{{ title }}</div>
        <div class="intro__illustration__description">
            <slot name='text'></slot>
        </div>
    </div>
</template>

<script setup>
const { title, customClass } = defineProps({
    img: String,
    title: String,
    customClass: String
})

</script>

<style></style>