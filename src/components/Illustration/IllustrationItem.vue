<template>
    <div :class="['illustration', `illustration--${customClass}`]">
        <div class='illustration__image'>
            <slot name="image"></slot>
        </div>
        <div class="illustration__title">{{ title }}</div>
        <div class="illustration__description">
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

<style lang='scss'>
.illustrations {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: map-get($spacings, 3x);
}

.illustration {
    display: flex;
    flex-direction: column;
    border-radius: 8px;
    border: 1px solid map-get($colors, neutral-200);
    background: map-get($background-colors, white);
    padding: map-get($spacings, 4x);

    &--purple {

        .illustration__image {
            background-color: map-get($background-colors, indigo-50);
        }
    }

    &--green {
        .illustration__image {
            background-color: map-get($background-colors, success-subtle);
        }
    }

    &--dark-purple {
        .illustration__image {
            background-color: map-get($background-colors, light-fushia);
        }
    }

    &--orange {
        .illustration__image {
            background-color: map-get($background-colors, warning-subtle);
        }
    }

    &__image {
        background-color: map-get($background-colors, indigo-50);
        border-radius: 8px;
        width: 40px;
        height: 40px;
        display: flex;
        justify-content: center;
        align-items: center;
        margin-bottom: map-get($spacings, 3x);
    }

    &__title {
        font-size: map-get($font-sizes, small);
        font-weight: map-get($font-weights, semibold);
        line-height: 20px;
        color: map-get($colors, neutral-900);
        margin-bottom: map-get($spacings, 2x);
    }

    &__description {
        font-size: map-get($font-sizes, xsmall);
        color: map-get($colors, neutral-600);
        font-weight: map-get($font-weights, normal);
        line-height: 16px;
    }

}
</style>