<template>
    <div class="chat-prompt">
        <!-- <textarea rows="1" placeholder="Ask me anything..." /> -->
        <chat-input></chat-input>
        <custom-button class='submit'>
            <img src="@/images/submit.svg" alt="send" />
            <span>Submit</span>
        </custom-button>
    </div>
</template>
<script setup>
import ChatInput from '../ChatInput/ChatInput.vue';
import CustomButton from '../CustomButton/CustomButton.vue';

</script>
<style lang='scss'>
.chat-prompt {
    display: flex;
    gap: 8px;

    .submit {
        align-self: end;
    }
}
</style>