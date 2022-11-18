<template>
  <header class="header">
    <div class="header__wrapper">
      <div class="row d-flex align-items-center">
        <div class="col mobile-hide">
          <CitySelect></CitySelect>
        </div>
        <div class="col mobile-hide">
          <SearchElement></SearchElement>
        </div>
        <div class="col">
          <div class="mobile-flex-between">
            <BurgerElement class="desktop-hide"></BurgerElement>
            <div class="logo">
              <img src="/mb_logo.svg" />
            </div>
            <BasketElement class="desktop-hide"></BasketElement>
          </div>
        </div>
        <div class="col mobile-hide">
          <BasketElement></BasketElement>
        </div>
        <div class="col mobile-hide">
          <AuthElement></AuthElement>
        </div>
      </div>
    </div>
  </header>
</template>
<script>
import CitySelect from '@/components/elements/CitySelect.vue'
import SearchElement from '@/components/elements/SearchElement.vue'
import BurgerElement from '@/components/elements/BurgerElement.vue'
import BasketElement from '@/components/elements/BasketElement.vue'
import AuthElement from '@/components/elements/AuthElement.vue'

export default {
  components: {
    CitySelect,
    SearchElement,
    BurgerElement,
    BasketElement,
    AuthElement
  }
}
</script>
<style>
.header {
  margin-bottom: 42px;
}
.header__wrapper {
  width: 1280px;
  margin: 0 auto;
}

@media (max-width: 780px) {
  .mobile-hide {
    display: none;
  }
  .header__wrapper {
    width: 100vw;
  }
  .header .row {
    margin: 0;
  }
  .header .col {
    padding: 0;
  }
  .header .logo {

  }
  .header .logo img {
    margin: 0 auto;
    display: block;
  }
  .mobile-flex-between {
    width: 100%;
    background-color: #000;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
}
</style>
