<template>
  <div>
    <PageHeader @menu-open="mobileMenuOpen()"></PageHeader>
    <div class="page__wrapper">
      <h1>Люксовые копии всемирных брендов</h1>
      <div class="h1__sub">Бесплатная доставка</div>
      <SearchElement class="desktop-hide"></SearchElement>
      <MobileMenu v-if="mobileMenu" @menu-close="mobileMenuClose()"></MobileMenu>
      <MainMenu></MainMenu>
      <CategoriesBig></CategoriesBig>
      <AdsOffer></AdsOffer>
      <SalesBig></SalesBig>
      <TrendsTopPopular></TrendsTopPopular>
      <AdTelegram></AdTelegram>
    </div>
  </div>
</template>

<script>
import PageHeader from '@/components/page/PageHeader.vue'
import MobileMenu from '@/components/page/MobileMenu.vue'
import MainMenu from '@/components/page/MainMenu.vue'
import CategoriesBig from '@/components/CategoriesBig.vue'
import AdsOffer from '@/components/ads/AdsOffer.vue'
import SalesBig from '@/components/SalesBig.vue'
import TrendsTopPopular from '@/components/TrendsTopPopular.vue'
import AdTelegram from '@/components/ads/AdTelegram.vue'
import SearchElement from "@/components/elements/SearchElement";

export default {
  name: 'IndexPage',
  layout: 'defaultLayout',
  components: {
    PageHeader,
    SearchElement,
    MobileMenu,
    MainMenu,
    CategoriesBig,
    AdsOffer,
    SalesBig,
    TrendsTopPopular,
    AdTelegram
  },
  data() {
    return {
      mobileMenu: false
    }
  },
  methods: {
    mobileMenuOpen() {
      this.mobileMenu = true
    },
    mobileMenuClose() {
      this.mobileMenu = false
    }
  }
}
</script>
<style>
.desktop-hide {
  display: none;
}
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

@media (max-width: 780px) {
  .desktop-hide {
    display: block;
  }
  h1 {
    font-size: 24px;
    line-height: 29px;
  }
  .h1__sub {
    margin-bottom: 30px;
  }
  .page__wrapper {
    width: 100vw;
  }
}
</style>
