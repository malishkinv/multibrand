<template>
  <div class="tpp">
    <div class="d-flex align-items-center tpp__menu">
      <div class="tpp__menu-item tpp__menu-item--active">Тренды</div>
      <div class="tpp__menu-item">Топ</div>
      <div class="tpp__menu-item">Популярное</div>
    </div>
    <div class="row">
      <div class="col">
        <div class="tpp__item">
          <div class="tpp__item-image">
            <img src="/tpp/tpp-1.png" />
          </div>
          <div class="tpp__item-info">
            <div class="tpp__item-price">4 320 ₽</div>
            <div class="tpp__item-brand">GUCCI</div>
            <div class="tpp__item-title">Футболка</div>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="tpp__item">
          <div class="tpp__item-image">
            <img src="/tpp/tpp-2.png" />
          </div>
          <div class="tpp__item-info">
            <div class="tpp__item-price">5 130 ₽</div>
            <div class="tpp__item-brand">LACOSTE</div>
            <div class="tpp__item-title">Толстовка</div>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="tpp__item">
          <div class="tpp__item-image">
            <img src="/tpp/tpp-3.png" />
          </div>
          <div class="tpp__item-info">
            <div class="tpp__item-price">11 610 ₽</div>
            <div class="tpp__item-brand">MONCLER</div>
            <div class="tpp__item-title">Куртка</div>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="tpp__item">
          <div class="tpp__item-image">
            <img src="/tpp/tpp-4.png" />
          </div>
          <div class="tpp__item-info">
            <div class="tpp__item-price">2 670 ₽</div>
            <div class="tpp__item-brand">STONE ISLAND</div>
            <div class="tpp__item-title">Сумка</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style>
.tpp {
  margin-bottom: 75px;
}
.tpp__menu {
  color: #000000;
  margin: 0 auto 40px;
  justify-content: center;
}
.tpp__menu-item {
  width: fit-content;
  text-align: center;
  font-style: normal;
  font-weight: 600;
  font-size: 24px;
  line-height: 29px;
  letter-spacing: 0.03em;
  color: #C1C1C1;
  margin-right: 54px;
  cursor: pointer;
}
.tpp__menu-item--active {
  color: #000000;
}
.tpp__menu-item:last-child {
  margin-right: 0;
}
.tpp__item-image {
  height: 270px;
  margin-bottom: 24px;
  cursor: pointer;
}
.tpp__item-info {
  cursor: pointer;
}
.tpp__item-price {
  margin-bottom: 8px;
  font-style: normal;
  font-weight: 600;
  font-size: 18px;
  line-height: 22px;
  letter-spacing: 0.03em;
  color: #000000;
}
.tpp__item-brand {
  margin-bottom: 8px;
  font-style: normal;
  font-weight: 700;
  font-size: 16px;
  line-height: 20px;
  letter-spacing: 0.03em;
  text-transform: uppercase;
  color: #000000;
}
.tpp__item-title {
  font-style: normal;
  font-weight: 300;
  font-size: 16px;
  line-height: 22px;
  color: #000000;
}
</style>
