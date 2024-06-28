<script setup lang="ts">
</script>

<template>
  <div class="container">
    <div class="login-section">
      <img class="login-section__logo" src="/logo.svg" width="205">
      <div class="login-section__title">Oturum aç</div>
      <div class="login-section__info">Aşağıdaki bilgileri doldurarak giriş yapabilirsiniz.</div>
      <div class="login-section__input">
        <input id="email" type="text" placeholder="E-posta">
        <label for="email">E-posta</label>
      </div>
      <div class="login-section__input">
        <input id="password" type="password" placeholder="Şifre">
        <label for="password">Şifre</label>
      </div>
      <div class="login-section__button">Giriş Yap</div>
      <div class="login-section__register">Henüz bir hesabınız yok mu?<span
          class="login-section__register--bold">Üye Ol</span></div>
      <div class="login-section__forgot">Şifremi unuttum</div>
    </div>
  </div>
</template>

<style lang="scss">
@import url('https://fonts.cdnfonts.com/css/sf-pro-display');

.container {
  width: 100%;
  height: 100%;
  background: url("/bg.png");
  display: flex;
  font-family: 'SF Pro Display', sans-serif;
  color: #000000;

  & .login-section {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    width: 33%;
    background: #FFFFFF;
    padding: 100px;
    box-sizing: border-box;

    &__title {
      font: normal normal bold 22px/26px SF Pro Display;
      margin-top: 55px;
      margin-bottom: 6px;
    }

    &__info {
      font: normal normal medium 16px/19px SF Pro Display;
      letter-spacing: 0px;
      color: #8F9BB3;
      opacity: 1;
      margin-bottom: 24px;
    }

    &__input {
      display: flex;
      align-items: stretch;
      margin-top: 6px;
      width: 100%;
      position: relative;
      & label {
        position: absolute;
        left: 20px;
        top: 8px;
        pointer-events: none;
        opacity: .5;
        color: #1676F8;
        font: normal normal 600 12px/14px SF Pro Display;
      }

      & input {
        width: 100%;
        background: #FFFFFF 0% 0% no-repeat padding-box;
        border: 1px solid #DFE1E6;
        border-radius: 10px;
        padding: 20px;
        color: #6B778C;

        &:focus {
          background: #F8F8F8;
          border: 1px solid #1676F8;
        }
      }

      input:placeholder-shown + label {
        opacity: 0;
      }
    }

    &__button {
      margin-top: 30px;
      background: #000000 0% 0% no-repeat padding-box;
      border-radius: 10px;
      opacity: 1;
      width: max-content;
      color: white;
      padding: 16px 20px;
    }

    &__register {
      margin-top: 44px;

      &--bold {
        margin-left: 10px;
        font: normal normal bold 16px/19px SF Pro Display;
      }
    }

    &__forgot {
      font: normal normal normal 16px/19px SF Pro Display;
      margin-top: 18px;
    }
  }
}
</style>
