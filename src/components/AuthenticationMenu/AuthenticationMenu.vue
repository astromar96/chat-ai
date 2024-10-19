<template>
    <div class="authenticate">
        <div class="authenticate__title">
            Let’s create an account
        </div>
        <div class="authenticate__description">
            Save your chat history, share chat, and personalize your experience.
        </div>
        <div class="authenticate__actions">
            <custom-button type='primary' full-width text='Sign in' />
            <custom-button type='link' full-width text='Create account' />
        </div>
    </div>
    <div class='user'>
        <div class="user__avatar">
            <img src="@/images/avatar.png" alt="user" />
            <span>John Doe</span>
        </div>
        <dropdown-menu>
            <div>
                <img src="@/images/settings.svg" alt="logo" />
                <span>Settings</span>
            </div>
            <div>
                <img src="@/images/logout.svg" alt="logo" />
                <span>Sign out</span>
            </div>
        </dropdown-menu>
    </div>
</template>
<script setup>
import CustomButton from '../CustomButton/CustomButton.vue';
import DropdownMenu from '../DropdownMenu/DropdownMenu.vue';
</script>

<style lang="scss">
.user {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-top: map-get($spacings, 4x);
    margin-bottom: map-get($spacings, 4x);
    padding: map-get($spacings, 3x);

    &__avatar {
        display: flex;
        align-items: center;
        gap: 6px;

        img {
            width: 20px;
            height: 20px;
            border-radius: 50%;
        }

        span {
            font-size: map-get($font-sizes, small);
            font-weight: map-get($font-weights, medium);
            line-height: 20px;
            color: map-get($colors, neutral-900);
        }
    }
}

.authenticate {
    border-radius: 8px;
    border: 1px solid map-get($colors, neutral-200);
    padding: map-get($spacings, 4x);
    margin-top: map-get($spacings, 4x);

    &__title {
        font-size: map-get($font-sizes, smail);
        font-weight: map-get($font-weights, medium);
        line-height: 20px;
        color: map-get($colors, neutral-900);
        margin-bottom: map-get($spacings, 2x);
    }

    &__description {
        font-size: map-get($font-sizes, xsmall);
        line-height: 16px;
        color: map-get($colors, neutral-600);
    }

    &__actions {
        display: flex;
        flex-direction: column;
        margin-top: map-get($spacings, 3x);
        text-align: center;
        gap: map-get($spacings, x);
    }
}
</style>