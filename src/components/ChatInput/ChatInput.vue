<template>
    <textarea :style="{ height }" @keyup='handleKeyUp' class="chat-input" placeholder="Type a message"></textarea>
</template>

<script setup>
import { ref } from 'vue';

const height = ref('40px');

const handleKeyUp = (event) => {
    height.value = `${calcHeight(event.target.value)}px`;
}

const calcHeight = (value) => {
    let numberOfLineBreaks = (value.match(/\n/g) || []).length;
    // min-height + lines x line-height + padding + border
    let newHeight = 20 + numberOfLineBreaks * 20 + 12 + 2;
    return newHeight;
}

</script>

<style lang='scss'>
.chat-input {
    flex: 1;
    -ms-overflow-style: none;
    scrollbar-width: none;
    max-height: 100px;
    border-radius: 8px;
    border: 1px solid map-get($colors, neutral-200);
    background-color: map-get($background-colors, neutral-50);
    height: 40px;
    padding: 12px 14px;
    outline: none;
    resize: none;
    transition: height 0.1s ease;
}
</style>