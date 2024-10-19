<template>
    <div :class="{
        'dropdown': true,
        'dropdown--open': isDropdownOpen
    }">
        <div class="dropdown__menu">
            <slot></slot>
        </div>
        <button @click='openDropdown' class="resetted-button">
            <img src="@/images/more-line.svg" alt="arrow" />
        </button>
    </div>
</template>

<script setup>
import { onMounted, ref } from 'vue';
const isDropdownOpen = ref(false);
const openDropdown = () => {
    isDropdownOpen.value = !isDropdownOpen.value;
}

onMounted(() => {
    document.body.addEventListener('click', (e) => {
        if (!e.target.closest('.dropdown')) {
            isDropdownOpen.value = false;
        }
    });
})
</script>

<style lang='scss'>
.dropdown {
    position: relative;

    &--open .dropdown__menu {
        display: block;
    }

    &__menu {
        display: none;
        position: absolute;
        width: 230px;
        bottom: 42px;
        padding: map-get($spacings, 2x);
        left: 0;
        border-radius: 8px;
        border: 1px solid map-get($colors, neutral-200);
        background: map-get($background-colors, white);
        /* shadow / shadow-md */
        box-shadow: 0px 4px 6px -1px rgba(0, 0, 0, 0.10), 0px 2px 4px -1px rgba(0, 0, 0, 0.06);

        &>div {
            display: flex;
            align-items: center;
            cursor: pointer;
            padding: map-get($spacings, 2x);
            gap: map-get($spacings, 3x);
            border-radius: 4px;
            color: map-get($colors, neutral-600);
            font-size: 14px;
            line-height: 20px;

            &:hover {
                background-color: map-get($background-colors, neutral-50);
                color: map-get($colors, neutral-950);
            }
        }
    }
}
</style>