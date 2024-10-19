<template>
    <div class="illustrations">
        <illustration-item title="Write an Essay" img='mail-open-line.svg' custom-class='purple'>
            <template v-slot:image>
                <img src="@/images/mail-open-line.svg" alt="pencil" />
            </template>
            <template v-slot:text>
                Generate email for any <br> occasion you need.
            </template>
        </illustration-item>
        <illustration-item title="Write an Essay" img='pencil-line.svg' custom-class='green'>
            <template v-slot:image>
                <img src="@/images/pencil-line.svg" alt="pencil" />
            </template>
            <template v-slot:text>
                Generate essay for any <br> occasion you need.
            </template>
        </illustration-item>
        <illustration-item title="Planning" img='timeline-view.svg' custom-class='dark-purple'>
            <template v-slot:image>
                <img src="@/images/timeline-view.svg" alt="timeline" />
            </template>
            <template v-slot:text>
                Plan for any occasion,<br> from holiday to family.
            </template>
        </illustration-item>
        <!-- .intro__illustration -->
        <illustration-item title="Planning" img='chat-1-line.svg' custom-class='orange'>
            <template v-slot:image>
                <img src="@/images/chat-1-line.svg" alt="chat" />
            </template>
            <template v-slot:text>
                Become your personal <br>assistant. Helping you.
            </template>
        </illustration-item>
        <!-- .intro__illustration -->
    </div>
</template>

<script setup>
import IllustrationItem from '../IllustrationItem/IllustrationItem.vue';

</script>

<style lang='scss'>
.illustrations {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: map-get($spacings, 3x);
}
</style>