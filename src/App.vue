<template>
  <div class="app">
    <div class="side-bar">
      <div class="side-bar__logo">
        <img src="@/images/logo.svg" alt="logo" />
        <span>Chat AI</span>
      </div>
      <!-- .side-bar__logo -->
      <div class="side-bar__active-prompts">
        <div class="side-bar__active-prompts__header">
          <img src="@/images/flashlight-line.svg" alt="logo" />
          <span>Ongoing prompt</span>
        </div>
      </div>
      <!-- .side-bar__active-prompts -->
      <custom-button left-aligned-content type='secondary'>
        <img src="@/images/sparkling-2-line.svg" alt="logo" />
        <span>Start new chat</span>
      </custom-button>
      <div class="side-bar__authenticate">
        <div class="side-bar__authenticate__title">
          Let’s create an account
        </div>
        <div class="side-bar__authenticate__description">
          Save your chat history, share chat, and personalize your experience.
        </div>
        <div class="side-bar__authenticate__actions">
          <custom-button type='primary' full-width text='Sign in' />
          <custom-button type='link' full-width text='Create account' />
        </div>
      </div>
      <div class='side-bar__user'>
        <div class="side-bar__user__avatar">
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
    </div>
    <div class="main">
      <div class="intro">
        <div class="intro__title">
          <strong>Hey, I’m Chat AI.</strong>
          <span>
            Your AI assistant and companion for any occasion.
          </span>
        </div>
        <!-- .intro__title -->
        <div class="intro__illustrations">
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
        <!-- .intro__illustrations -->
      </div>
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
import CustomButton from './components/Button/CustomButton.vue';
import DropdownMenu from './components/Dropdown/DropdownMenu.vue';
import IllustrationItem from './components/Illustration/IllustrationItem.vue';

</script>
<style lang='scss'>
.app {
  display: flex;
  height: 100vw;
  max-height: 100vh;
}

.side-bar {
  width: 240px;
  border-right: 1px solid map-get($colors, neutral-200);
  padding: map-get($spacings, 3x) map-get($spacings, 4x);
  user-select: none;
  display: flex;
  flex-direction: column;

  &__user {
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

  &__logo {
    display: flex;
    align-items: center;
    padding: map-get($spacings, 4x) map-get($spacings, 2x);
  }

  &__active-prompts {
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

  &__authenticate {
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
}

.main {
  flex: 1;
  padding: 80px 180px 24px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  max-height: 100vh;
}

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
