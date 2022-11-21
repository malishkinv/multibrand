<template>
  <div class="burger" @click="mobileMenuOpen()"></div>
</template>

<script>
export default {
  methods: {
    mobileMenuOpen() {
      this.$emit('menu-open')
    }
  }
}
</script>
<style>
.burger {
  background-image: url(/icons/icon__burger.svg);
  background-repeat: no-repeat;
  background-position: 0 50%;
  background-size: 14px 20px;
  width: 20px;
  height: 16px;
  margin: 0 auto;
  cursor: pointer;
}
</style>
