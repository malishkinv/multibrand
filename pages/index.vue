<template>
  <div class="page__wrapper">
    <h1>Люксовые копии всемирных брендов</h1>
    <div class="h1__sub">Бесплатная доставка</div>
    <MainMenu></MainMenu>
    <CategoriesBig></CategoriesBig>
    <AdsOffer></AdsOffer>
    <SalesBig></SalesBig>
    <TrendsTopPopular></TrendsTopPopular>
    <AdTelegram></AdTelegram>
  </div>
</template>

<script>
import MainMenu from '@/components/page/MainMenu.vue'
import CategoriesBig from '@/components/CategoriesBig.vue'
import AdsOffer from '@/components/ads/AdsOffer.vue'
import SalesBig from '@/components/SalesBig.vue'
import TrendsTopPopular from '@/components/TrendsTopPopular.vue'
import AdTelegram from '@/components/ads/AdTelegram.vue'

export default {
  name: 'IndexPage',
  layout: 'defaultLayout',
  components: {
    MainMenu,
    CategoriesBig,
    AdsOffer,
    SalesBig,
    TrendsTopPopular,
    AdTelegram
  }
}
</script>
<style>
.page__wrapper {
  width: 1280px;
  margin: 0 auto;
}
h1 {
  text-align: center;
  font-weight: 600;
  font-size: 32px;
  line-height: 39px;
  letter-spacing: 0.03em;
  color: #000000;
}
.h1__sub {
  margin-top: 8px;
  font-weight: 300;
  font-size: 16px;
  line-height: 22px;
  color: #000000;
  text-align: center;
  margin-bottom: 40px;
}
</style>
