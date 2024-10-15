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
      <div class="side-bar__start-new-chat">
        <img src="@/images/sparkling-2-line.svg" alt="logo" />
        <span class="side-bar__start-new-chat__text">Start new chat</span>
      </div>
      <!-- .side-bar__start-new-chat -->
      <div class="side-bar__authenticate">
        <div class="side-bar__authenticate__title">
          Let’s create an account
        </div>
        <div class="side-bar__authenticate__description">
          Save your chat history, share chat, and personalize your experience.
        </div>
        <div class="side-bar__authenticate__actions">
          <div class="side-bar__authenticate__actions__signin">
            Sign in
          </div>
          <div class="side-bar__authenticate__actions__signup">
            Create account
          </div>
        </div>
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
          <div class="intro__illustration intro__illustration--purple">
            <div class='intro__illustration__image'>
              <img src="@/images/mail-open-line.svg" alt="illustration" />
            </div>
            <div class="intro__illustration__title">Get instant answers</div>
            <div class="intro__illustration__description">
              Generate email for any <br> occasion you need.
            </div>
          </div>
          <!-- .intro__illustration -->
          <div class="intro__illustration intro__illustration--green">
            <div class='intro__illustration__image'>
              <img src="@/images/pencil-line.svg" alt="illustration" />
            </div>
            <div class="intro__illustration__title">Write an Essay</div>
            <div class="intro__illustration__description">
              Generate essay for any <br> occasion you need.
            </div>
          </div>
          <!-- .intro__illustration -->
          <div class="intro__illustration intro__illustration--dark-purple">
            <div class='intro__illustration__image'>
              <img src="@/images/timeline-view.svg" alt="illustration" />
            </div>
            <div class="intro__illustration__title">Planning</div>
            <div class="intro__illustration__description">
              Plan for any occasion,<br> from holiday to family.
            </div>
          </div>
          <!-- .intro__illustration -->
          <div class="intro__illustration intro__illustration--orange">
            <div class='intro__illustration__image'>
              <img src="@/images/chat-1-line.svg" alt="illustration" />
            </div>
            <div class="intro__illustration__title">Assistant</div>
            <div class="intro__illustration__description">
              Become your personal <br>assistant. Helping you.
            </div>
          </div>
          <!-- .intro__illustration -->
        </div>
        <!-- .intro__illustrations -->
      </div>
      <!-- .intro -->
      <div class="chat-prompt">
        <textarea rows="1" placeholder="Ask me anything..." />
        <button class="button">
          <img src="@/images/submit.svg" alt="send" />
          <span>Submit</span>
        </button>
      </div>
    </div>
    <!-- .main -->
  </div>
</template>
<script setup>

</script>
<style lang='scss'>
.app {
  display: flex;
  height: 100vw;
  max-height: 100vh;
}

.side-bar {
  width: 240px;
  border-right: 1px solid map-get($colors, light-gray);
  padding: map-get($spacings, 3x) map-get($spacings, 2x);
  user-select: none;

  &__logo {
    display: flex;
    align-items: center;
    padding: map-get($spacings, 2x) map-get($spacings, half-x);
  }

  &__active-prompts {
    height: 396px;

    &__header {
      display: flex;
      align-items: center;
      padding: map-get($spacings, third-x);
      gap: map-get($spacings, x-and-half);
      background-color: map-get($background-colors, tertiary);
      border-radius: 4px;
      color: map-get($colors, brand);
    }
  }

  &__start-new-chat {
    display: flex;
    align-items: center;
    padding: 10px;
    border-radius: 4px;
    border: 0.5px solid map-get($colors, light-gray);
    box-shadow: 0px 1px 3px 0px rgba(0, 0, 0, 0.10), 0px 1px 2px 0px rgba(0, 0, 0, 0.06);
    cursor: pointer;
    gap: map-get($spacings, half-x);

    &__text {
      color: map-get($colors, primary);
      font-size: map-get($font-sizes, small);
      font-weight: map-get($font-weights, medium);
      line-height: 20px;
    }
  }

  &__authenticate {
    border-radius: 8px;
    border: 1px solid map-get($colors, light-gray);
    padding: map-get($spacings, 2x);
    margin-top: map-get($spacings, 2x);

    &__title {
      font-size: map-get($font-sizes, smail);
      font-weight: map-get($font-weights, medium);
      line-height: 20px;
      color: map-get($colors, primary);
      margin-bottom: map-get($spacings, half-x);
    }

    &__description {
      font-size: map-get($font-sizes, xsmall);
      line-height: 16px;
      color: map-get($colors, secondary);
    }

    &__actions {
      margin-top: map-get($spacings, 3x);
      text-align: center;

      &__signin {
        cursor: pointer;
        color: map-get($colors, primary-invert);
        border-radius: 4px;
        background: map-get($background-colors, brand);
        box-shadow: 0px 1px 3px 0px rgba(0, 0, 0, 0.10), 0px 1px 2px 0px rgba(0, 0, 0, 0.06);
        padding: map-get($spacings, x);
        margin-bottom: map-get($spacings, half-x);
      }

      &__signup {
        cursor: pointer;
        border-radius: 4px;
        padding: map-get($spacings, x);
        color: map-get($colors, brand);
        font-size: map-get($font-sizes, small);
        font-weight: map-get($font-weights, medium);
        line-height: 20px;
      }
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
      color: map-get($colors, secondary);
    }
  }

  &__illustrations {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: map-get($spacings, 3x);
  }

  &__illustration {
    display: flex;
    flex-direction: column;
    border-radius: 8px;
    border: 1px solid map-get($colors, light-gray);
    background: map-get($background-colors, primary);
    padding: map-get($spacings, 2x);

    &--purple {

      .intro__illustration__image {
        background-color: map-get($background-colors, light-purple);
      }
    }

    &--green {
      .intro__illustration__image {
        background-color: map-get($background-colors, success-subtle);
      }
    }

    &--dark-purple {
      .intro__illustration__image {
        background-color: map-get($background-colors, light-fushia);
      }
    }

    &--orange {
      .intro__illustration__image {
        background-color: map-get($background-colors, warning-subtle);
      }
    }

    &__image {
      background-color: map-get($background-colors, light-purple);
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
      color: map-get($colors, primary);
      margin-bottom: map-get($spacings, x);
    }

    &__description {
      font-size: map-get($font-sizes, xsmall);
      color: map-get($colors, secondary);
      font-weight: map-get($font-weights, normal);
      line-height: 16px;
    }
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
    border: 1px solid map-get($colors, light-gray);
    background-color: map-get($background-colors, tertiary);
    height: 40px;
    padding: 12px 14px;
    outline: none;
    resize: none;
  }

  button {
    display: flex;
    padding: 10px 14px;
    justify-content: center;
    align-items: center;
    gap: 4px;
    border-radius: 4px;
    background: map-get($background-colors, brand);
    color: map-get($colors, primary-invert);
  }
}
</style>
