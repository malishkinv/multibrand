<template>
  <div class="city__select">
    <span class="city__select-selected">Москва</span>
  </div>
</template>
<style>
.city__select {
  background-image: url(/icons/icon__location.svg);
  background-repeat: no-repeat;
  background-position: 0 50%;
  background-size: 15px 20px;
  position: relative;
  width: fit-content;
  padding-right: 18px;
  cursor: pointer;
}
.city__select:after {
  content: '';
  position: absolute;
  width: 8px;
  height: 4px;
  right: 0;
  top: 50%;
  margin-top: -2px;
  background-image: url(/icons/icon__dropdown.svg);
  background-repeat: no-repeat;
  background-size: 8px 4px;
}
.city__select-selected {
  font-size: 16px;
  color: #000;
  padding-left: 32px;
}
</style>
