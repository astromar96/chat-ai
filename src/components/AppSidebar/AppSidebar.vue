<template>
    <div class="side-bar">
        <div class="side-bar__logo">
            <img src="@/images/logo.svg" alt="logo" />
            <span>Chat AI</span>
        </div>
        <!-- .side-bar__logo -->
        <chat-history></chat-history>
        <!-- .side-bar__active-prompts -->
        <custom-button left-aligned-content type='secondary'>
            <img src="@/images/sparkling-2-line.svg" alt="logo" />
            <span>Start new chat</span>
        </custom-button>
        <authentication-menu></authentication-menu>
    </div>
</template>
<script setup>
import AuthenticationMenu from '../AuthenticationMenu/AuthenticationMenu.vue';
import ChatHistory from '../ChatHistory/ChatHistory.vue';
import CustomButton from '../CustomButton/CustomButton.vue';

</script>
<style lang="scss">
.side-bar {
    width: 240px;
    border-right: 1px solid map-get($colors, neutral-200);
    padding: map-get($spacings, 3x) map-get($spacings, 4x);
    user-select: none;
    display: flex;
    flex-direction: column;

    &__logo {
        display: flex;
        align-items: center;
        padding: map-get($spacings, 4x) map-get($spacings, 2x);
    }
}
</style>