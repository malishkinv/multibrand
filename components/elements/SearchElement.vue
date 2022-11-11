<template>
  <div>
    <input type="search" placeholder="Поиск" class="form-control form__search" />
  </div>
</template>
<style>
.form__search {
  border: none;
  border-bottom: 1px solid grey;
  border-radius: 0;
  font-size: 16px;
  padding-left: 0;
  margin: 0 auto;
  max-width: 184px;
  outline: none;

  background-image: url(/icons/icon__search.svg);
  background-size: 18px;
  background-position: 100% 50%;
  background-repeat: no-repeat;
}
.form__search::placeholder {
  color: #000;
}
</style>
