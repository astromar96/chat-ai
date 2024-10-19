<template>
    <div class="intro">
        <div class="intro__title">
            <strong>Hey, I’m Chat AI.</strong>
            <span>
                Your AI assistant and companion for any occasion.
            </span>
        </div>
        <!-- .intro__title -->
        <illustration-items></illustration-items>
    </div>
</template>
<script setup>
import IllustrationItems from '../IllustrationItems/IllustrationItems.vue';

</script>
<style lang='scss'>
.intro {
    &__title {
        font-size: map-get($font-sizes, xxlarge);
        font-weight: map-get($font-weights, medium);
        line-height: 36px;
        margin-bottom: 80px;

        span {
            color: map-get($colors, neutral-600);
        }
    }

    &__illustrations {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        gap: map-get($spacings, 3x);
    }
}
</style>