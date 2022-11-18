<template>
  <div class="ads__offer">
    <div class="row h-100">
      <div class="col h-100">
        <div class="ads__offer-left">
          <img src="/ads/ads__offer-left.png" />
          <div class="mobile-price-bottom">
            <div class="ads__offer-left--price">128 000 ₽</div>
          </div>
        </div>
      </div>
      <div class="col d-flex flex-column align-items-center justify-content-center h-100">
        <h2 class="ads__offer-title">Пришлем копию<br />любого товара</h2>
        <div class="ads__offer-text">Покажите, какой товар Вы хотите,<br />и мы пришлём люксовую копию,<br />которую Вы не отличите от оригинала.</div>
        <div class="ads__offer-button">Написать заявку</div>
      </div>
      <div class="col h-100">
        <div class="ads__offer-right">
          <img src="/ads/ads__offer-right.png" />
          <div class="mobile-price-bottom">
            <div class="ads__offer-right--price">6 700 ₽</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style>
.ads__offer {
  margin-bottom: 75px;
  height: 350px;
  background: radial-gradient(40.29% 40.29% at 34.5% 3.71%, #F6F6F6 0%, #E7E7E7 100%);
}
.ads__offer-title {
  margin-bottom: 20px;
  font-style: normal;
  font-weight: 600;
  font-size: 32px;
  line-height: 39px;
  text-align: center;
  letter-spacing: 0.03em;
  color: #000000;
}
.ads__offer-text {
  font-style: normal;
  font-weight: 600;
  font-size: 18px;
  line-height: 25px;
  text-align: center;
  color: #000000;
  margin-bottom: 32px;
}
.ads__offer-button {
  padding: 15px 25px;
  font-style: normal;
  font-weight: 600;
  font-size: 14px;
  line-height: 17px;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: #FFFFFF;
  text-align: center;
  background-color: #000;
  width: fit-content;
  margin: 0 auto;
  cursor: pointer;
}
.ads__offer-left {
  position: relative;
}
.ads__offer-left--price {
  position: absolute;
  top: 52px;
  right: 70px;
  font-style: normal;
  font-weight: 600;
  font-size: 18px;
  line-height: 22px;
  letter-spacing: 0.03em;
  color: #000000;
  padding: 5px 15px;
  background-color: #fff;
}
.ads__offer-right {
  position: relative;
}
.ads__offer-right--price {
  position: absolute;
  top: 56px;
  left: 28px;
  font-style: normal;
  font-weight: 600;
  font-size: 18px;
  line-height: 22px;
  letter-spacing: 0.03em;
  color: #000000;
  padding: 5px 15px;
  background-color: #fff;
}

@media (max-width: 780px) {
  .ads__offer {
    height: auto;
    margin-bottom: 40px;
    padding-top: 15px;
    padding-bottom: 40px;
  }
  .ads__offer .row {
    margin: 0;
  }
  .ads__offer .col {
    padding: 0;
  }
  .ads__offer .col:nth-child(1) {
    order: 1;
    width: 50%;
    min-width: 50%;
    padding: 0 18px;
  }
  .ads__offer .col:nth-child(3) {
    order: 2;
    width: 50%;
    min-width: 50%;
    padding: 0 18px;
  }
  .ads__offer .col:nth-child(2) {
    order: 3;
    width: 100%;
    min-width: 100%;
    margin-top: 28px;
  }
  .ads__offer-title {
    font-size: 24px;
    line-height: 29px;
    margin-bottom: 20px;
  }
  .ads__offer-text {
    font-size: 16px;
    line-height: 22px;
    margin-bottom: 20px;
  }
  .ads__offer-left, .ads__offer-right {
    height: 233px;
    display: flex;
    align-items: center;
    border: 1px solid #fff;
  }
  .ads__offer-left img, .ads__offer-right img {
    width: 100%;
    display: block;
    margin: auto;
  }
  .ads__offer-left--price, .ads__offer-right--price {
    font-size: 16px;
    line-height: 20px;
    position: relative;
    top: auto;
    bottom: auto;
    left: auto;
    right: auto;
  }
  .mobile-price-bottom {
    position: absolute;
    bottom: 0;
    width: 100%;
    display: flex;
    justify-content: center;
  }
}
</style>
