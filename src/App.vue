<template>
  <div class="app">
    <app-sidebar></app-sidebar>
    <div class="main">
      <app-intro></app-intro>
      <!-- .intro -->
      <chat-prompt></chat-prompt>
    </div>
    <!-- .main -->
  </div>
</template>
<script setup>
import AppIntro from './components/AppIntro/AppIntro.vue';
import AppSidebar from './components/AppSidebar/AppSidebar.vue';
import ChatPrompt from './components/ChatPrompt/ChatPrompt.vue';
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

  .submit {
    align-self: end;
  }
}
</style>
