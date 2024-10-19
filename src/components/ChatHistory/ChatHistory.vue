<template>
    <div class="active-prompts">
        <div class="active-prompts__header">
            <img src="@/images/flashlight-line.svg" alt="logo" />
            <span>Ongoing prompt</span>
        </div>
        <div class="past-prompts">
            <span class="past-prompts__title">Past</span>
            <div class="past-prompts__item past-prompts__item--active">
                <svg width="20" height="20" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                    <g id="file-list-2-line">
                        <path id="Vector"
                            d="M16.6667 18.3334H3.33333C2.8731 18.3334 2.5 17.9603 2.5 17.5001V2.50008C2.5 2.03985 2.8731 1.66675 3.33333 1.66675H16.6667C17.1269 1.66675 17.5 2.03985 17.5 2.50008V17.5001C17.5 17.9603 17.1269 18.3334 16.6667 18.3334ZM15.8333 16.6667V3.33341H4.16667V16.6667H15.8333ZM6.66667 5.83341H13.3333V7.50008H6.66667V5.83341ZM6.66667 9.16675H13.3333V10.8334H6.66667V9.16675ZM6.66667 12.5001H10.8333V14.1667H6.66667V12.5001Z" />
                    </g>
                </svg>

                <span class="past-prompts__item__title">What is the weather today?</span>
            </div>

            <div class="past-prompts__item">
                <svg width="20" height="20" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                    <g id="file-list-2-line">
                        <path id="Vector"
                            d="M16.6667 18.3334H3.33333C2.8731 18.3334 2.5 17.9603 2.5 17.5001V2.50008C2.5 2.03985 2.8731 1.66675 3.33333 1.66675H16.6667C17.1269 1.66675 17.5 2.03985 17.5 2.50008V17.5001C17.5 17.9603 17.1269 18.3334 16.6667 18.3334ZM15.8333 16.6667V3.33341H4.16667V16.6667H15.8333ZM6.66667 5.83341H13.3333V7.50008H6.66667V5.83341ZM6.66667 9.16675H13.3333V10.8334H6.66667V9.16675ZM6.66667 12.5001H10.8333V14.1667H6.66667V12.5001Z" />
                    </g>
                </svg>

                <span class="past-prompts__item__title">What is the weather today?</span>
            </div>
        </div>
    </div>
</template>
<style lang='scss'>
.active-prompts {
    height: 396px;
    flex-grow: 1;

    &__header {
        display: flex;
        align-items: center;
        padding: 6px;
        gap: map-get($spacings, 3x);
        background-color: map-get($background-colors, neutral-50);
        border-radius: 4px;
        color: map-get($colors, indigo-700);
    }
}

.past-prompts {

    &__title {
        display: block;
        padding: map-get($spacings, x);
        font-size: map-get($font-sizes, small);
        font-weight: map-get($font-weights, medium);
        line-height: 20px;
        color: map-get($colors, neutral-600);
        margin-top: map-get($spacings, 3x);
        margin-bottom: map-get($spacings, x);
    }

    &__item {
        display: flex;
        align-items: center;
        gap: map-get($spacings, 3x);
        padding: map-get($spacings, 2x);
        border-radius: 4px;
        font-size: map-get($font-sizes, small);
        font-weight: map-get($font-weights, medium);
        line-height: 20px;
        margin-bottom: map-get($spacings, 2x);
        color: map-get($colors, neutral-600);
        cursor: pointer;

        &:hover {
            background-color: map-get($background-colors, neutral-50);
        }

        svg {
            fill: map-get($colors, neutral-600);
        }

        &--active {
            background-color: map-get($background-colors, neutral-50);
            color: map-get($colors, indigo-700);
            cursor: default;

            svg {
                fill: map-get($colors, indigo-700);
            }
        }

        &__title {
            flex: 1;
            white-space: nowrap;
            overflow: hidden;
            display: block;
            text-overflow: ellipsis;
        }
    }

}
</style>