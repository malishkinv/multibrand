<template>
  <div class="categories__big d-flex">
    <div class="col">
      <div class="categories__big-item categories__big-item--women">
        <div class="categories__big-caption">Для женщин</div>
      </div>
    </div>
    <div class="col">
      <div class="categories__big-item categories__big-item--men">
        <div class="categories__big-caption">Для мужчин</div>
      </div>
    </div>
    <div class="col">
      <div class="categories__big-item categories__big-item--kids">
        <div class="categories__big-caption">Для детей</div>
      </div>
    </div>
  </div>
</template>
<style>
.categories__big {
  height: 585px;
  margin-bottom: 75px;
}
.categories__big-item {
  height: 100%;
  background-position: 50%;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
  cursor: pointer;
}
.categories__big-item:after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  opacity: 0;
}
.categories__big-item:hover:after {
  opacity: 1;
  transition: opacity 0.2s;
  background: rgba(0, 0, 0, 0.5);
}
.categories__big-item--women {
  background-image: url(/categories/categories__big-1.png);
}
.categories__big-item--men {
  background-image: url(/categories/categories__big-2.png);
}
.categories__big-item--kids {
  background-image: url(/categories/categories__big-3.png);
}
.categories__big-caption {
  position: absolute;
  bottom: 0;
  left: 50%;
  margin-left: -98px;
  width: 186px;
  background-color: #000;
  font-style: normal;
  font-weight: 600;
  font-size: 14px;
  line-height: 17px;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: #FFFFFF;
  padding: 12px 0;
  text-align: center;
}

@media (max-width: 780px) {
  .categories__big {
    height: 453px;
    max-width: 100vw;
    overflow: auto;
    margin-bottom: 40px;
  }
  .categories__big .col {
    min-width: 80%;
    max-width: 80%;
    padding: 0;
    margin-right: 9px;
  }

  .categories__big .col:last-child {
    margin-right: 0;
  }
}
</style>
