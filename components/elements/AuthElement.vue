<template>
  <div class="auth" :class="{'auth--mobile': mobile}">Войти</div>
</template>

<script>
export default {
  props: {
    mobile: { type: Boolean, default: false }
  }
}
</script>
<style>
.auth {
  background-image: url(/icons/icon__signin.svg);
  background-repeat: no-repeat;
  background-position: 0 50%;
  background-size: 14px 19px;
  padding-left: 28px;
  font-size: 16px;
  color: #000;
  width: fit-content;
  margin: 0 0 0 auto;
  cursor: pointer;
}
.auth--mobile {
  background-image: url(/icons/icon__signin-mobile.svg);
  color: #fff;
  margin: 0;
}
</style>
