<template>
  <div class="sales__big row">
    <div class="col">
      <div class="sales__big-item">
        <div class="sales__big-item-badge-new">NEW</div>
        <div class="sales__big-item-image">
          <img src="/sales/sales__big-1.png" />
        </div>
        <div class="sales__big-item-info">
          <div class="sales__big-item-price">18 900 ₽</div>
          <div class="sales__big-item-brand">DIOR</div>
          <div class="sales__big-item-title">Пуховик</div>
        </div>
      </div>
    </div>
    <div class="col">
      <div class="sales__big-item">
        <div class="sales__big-item-badge-new">NEW</div>
        <div class="sales__big-item-image">
          <img src="/sales/sales__big-2.png" />
        </div>
        <div class="sales__big-item-info">
          <div class="sales__big-item-price">3 780 ₽</div>
          <div class="sales__big-item-brand">SUPREME</div>
          <div class="sales__big-item-title">Рюкзак</div>
        </div>
      </div>
    </div>
  </div>
</template>
<style>
.sales__big {
  margin-bottom: 75px;
}
.sales__big-item {
  position: relative;
  cursor: pointer;
}
.sales__big-item-badge-new {
  position: absolute;
  padding: 5px;
  background-color: #000;
  font-style: normal;
  font-weight: 600;
  font-size: 12px;
  line-height: 15px;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: #FFFFFF;
  text-align: center;
}
.sales__big-item-image {
  height: 580px;
  margin-bottom: 24px;
}
.sales__big-item-info {}
.sales__big-item-price {
  margin-bottom: 8px;
  font-style: normal;
  font-weight: 600;
  font-size: 18px;
  line-height: 22px;
  letter-spacing: 0.03em;
  color: #000000;
}
.sales__big-item-brand {
  margin-bottom: 8px;
  font-style: normal;
  font-weight: 700;
  font-size: 16px;
  line-height: 20px;
  letter-spacing: 0.03em;
  text-transform: uppercase;
  color: #000000;
}
.sales__big-item-title {
  font-style: normal;
  font-weight: 300;
  font-size: 16px;
  line-height: 22px;
  color: #000000;
}
</style>
