<template>
  <div class="app">
    <app-sidebar></app-sidebar>
    <div class="main">
      <app-intro></app-intro>
      <!-- .intro -->
      <div class="chat-prompt">
        <textarea rows="1" placeholder="Ask me anything..." />
        <custom-button>
          <img src="@/images/submit.svg" alt="send" />
          <span>Submit</span>
        </custom-button>
      </div>
    </div>
    <!-- .main -->
  </div>
</template>
<script setup>
import AppIntro from './components/AppIntro/AppIntro.vue';
import AppSidebar from './components/AppSidebar/AppSidebar.vue';
import CustomButton from './components/CustomButton/CustomButton.vue';

</script>
<style lang='scss'>
.app {
  display: flex;
  height: 100vw;
  max-height: 100vh;
}

.main {
  flex: 1;
  padding: 80px 180px 24px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  max-height: 100vh;
}



.chat-prompt {
  display: flex;
  gap: 8px;

  textarea {
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
  }
}
</style>
