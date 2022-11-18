<template>
  <div class="sales__big row mobile-column">
    <div class="col">
      <div class="sales__big-item sales__big-item--left">
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
      <div class="sales__big-item sales__big-item--right">
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
  width: fit-content;
  margin: 0 auto;
  padding: 10px;
  transition: all .2s;
}
.sales__big-item--left {
  margin-right: 25px;
}
.sales__big-item--right {
  margin-left: 25px;
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

@media (min-width: 780px) {
  .sales__big-item:hover {
    box-shadow: 0 7px 15px rgba(0, 0, 0, 0.2);
  }
}
@media (max-width: 780px) {
  .mobile-column {
    flex-direction: column;
  }
  .sales__big-item {
    margin: 0 auto 24px !important;
    padding: 0 18px;
  }
  .sales__big .col {
    padding: 0;
  }
  .sales__big.row {
    margin: 0;
  }
  .sales__big-item--left {
    margin-right: 0;
  }
  .sales__big-item--right {
    margin-left: 0;
  }
  .sales__big-item-image {
    height: auto;
    width: 100%;
  }
  .sales__big-item-image img {
    width: 100%;
  }
}
</style>
