<template>
  <div class="d-flex align-items-center mainmenu">
    <div class="mainmenu__item">Одежда</div>
    <div class="mainmenu__item">Обувь</div>
    <div class="mainmenu__item">Аксессуары</div>
    <div class="mainmenu__item">Бренды</div>
    <div class="mainmenu__item">Sale%</div>
  </div>
</template>
<style>
.mainmenu {
  color: #000000;
  margin: 0 auto;
  justify-content: center;
  margin-bottom: 30px;
}
.mainmenu__item {
  width: fit-content;
  text-align: center;
  font-style: normal;
  font-weight: 500;
  font-size: 18px;
  line-height: 22px;
  margin-right: 54px;
  cursor: pointer;
}
.mainmenu__item:last-child {
  margin-right: 0;
}
</style>
