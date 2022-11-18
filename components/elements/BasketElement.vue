<template>
  <div class="basket"><span class="mobile-hide">Корзина</span></div>
</template>
<style>
.basket {
  padding-left: 28px;
  background-image: url(/icons/icon__basket.svg);
  background-repeat: no-repeat;
  background-position: 0 50%;
  background-size: 14px 20px;
  font-size: 16px;
  color: #000;
  width: fit-content;
  margin: 0 auto;
  cursor: pointer;
}
@media (max-width: 780px) {
  .basket {
    padding: 0;
    background-image: url(/icons/icon__basket-mobile.svg);
    width: 14px;
    height: 20px;
  }
}
</style>
