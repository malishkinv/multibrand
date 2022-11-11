<template>
  <header class="header">
    <div class="header__wrapper">
      <div class="row d-flex align-items-center">
        <div class="col">
          <CitySelect></CitySelect>
        </div>
        <div class="col">
          <SearchElement></SearchElement>
        </div>
        <div class="col">
          <div class="logo">
            <img src="/mb_logo.svg" />
          </div>
        </div>
        <div class="col">
          <BasketElement></BasketElement>
        </div>
        <div class="col">
          <AuthElement></AuthElement>
        </div>
      </div>
    </div>
  </header>
</template>
<script>
import CitySelect from '@/components/elements/CitySelect.vue'
import SearchElement from '@/components/elements/SearchElement.vue'
import BasketElement from '@/components/elements/BasketElement.vue'
import AuthElement from '@/components/elements/AuthElement.vue'

export default {
  components: {
    CitySelect,
    SearchElement,
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
</style>
