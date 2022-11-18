<template>
  <div class="ads__telegram">
    <img class="ads__telegram-icon" src="/icons/icon__telegram-big.svg" />
    <div class="ads__telegram-text">Консультации, продажи<br />@mltbrandsale</div>
  </div>
</template>
<style>
.ads__telegram {
  padding: 42px 0;
  background: radial-gradient(40.29% 40.29% at 34.5% 3.71%, #F6F6F6 0%, #E7E7E7 100%);
}
.ads__telegram-icon {
  display: block;
  margin: 0 auto 20px;
}
.ads__telegram-text {
  font-style: normal;
  font-weight: 600;
  font-size: 24px;
  line-height: 150%;
  text-align: center;
  letter-spacing: 0.03em;
  color: #000000;
}

@media (max-width: 780px) {
  .ads__telegram-text {
    font-size: 18px;
    line-height: 27px;
  }
}
</style>
