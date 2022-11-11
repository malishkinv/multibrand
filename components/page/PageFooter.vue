<template>
  <footer class="footer">
    <div class="footer__wrapper">
      <div class="row">
      <div class="col-7 d-flex">
        <div class="footer__menu">
          <div class="footer__menu-item">О нас</div>
          <div class="footer__menu-item">Оплата</div>
          <div class="footer__menu-item">Доставка</div>
          <div class="footer__menu-item">Как заказать</div>
          <div class="footer__menu-item">Контакты</div>
        </div>
        <div class="footer__menu">
          <div class="footer__menu-item">Одежда</div>
          <div class="footer__menu-item">Обувь</div>
          <div class="footer__menu-item">Аксессуары</div>
          <div class="footer__menu-item">Бренды</div>
          <div class="footer__menu-item">Sale%</div>
        </div>
        <div class="footer__menu">
          <div class="footer__menu-item">Мои заказы</div>
          <div class="footer__menu-item">Возврат</div>
          <div class="footer__menu-item">Публичная оферта</div>
          <div class="footer__menu-item">Часто задаваемые вопросы</div>
        </div>
      </div>
      <div class="col-5 d-flex justify-content-end">
        <div class="footer__contacts">
          <div class="footer__contacts-tel">+7 (495) 879-87-88</div>
          <div class="footer__contacts-socials d-flex justify-content-end">
            <div class="footer__contacts-social footer__contacts-social--tg"></div>
            <div class="footer__contacts-social footer__contacts-social--vk"></div>
            <div class="footer__contacts-social footer__contacts-social--fb"></div>
            <div class="footer__contacts-social footer__contacts-social--ig"></div>
          </div>
          <div class="footer__contacts-contact-us">Связаться с нами</div>
        </div>
      </div>
    </div>
    </div>
    <div class="footer__copyright">
      <div class="footer__wrapper">
        <div class="row justify-content-between">
          <div class="col-8">
            <a href="#">Политика конфиденциальности</a> &nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp; <a href="#">Политика обработки персональных данных</a>
          </div>
          <div class="col-4 d-flex justify-content-end">
            © Мультибрендовый
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>
<style>
.footer {
  margin-top: 120px;
}
.footer__wrapper {
  width: 1280px;
  margin: 0 auto;
}
.footer__copyright {
  margin-top: 120px;
  background-color: #000;
  padding: 28px 0;
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 150%;
  color: #F9F9F9;
}
.footer__copyright a {
  color: #fff;
  text-decoration: underline;
}
.footer__menu {
  margin-right: 136px;
}
.footer__menu:last-child {
  margin-right: 0;
}
.footer__menu-item {
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 22px;
  color: #000000;
  margin-bottom: 20px;
  cursor: pointer;
}
.footer__menu-item:last-child {
  margin-bottom: 0;
}
.footer__contacts {}
.footer__contacts-tel {
  font-style: normal;
  font-weight: 700;
  font-size: 20px;
  line-height: 27px;
  color: #000000;
  margin-bottom: 32px;
}
.footer__contacts-socials {
  margin-bottom: 40px;
}
.footer__contacts-social {
  width: 30px;
  height: 30px;
  margin-right: 16px;
  background-size: 30px;
  background-repeat: no-repeat;
  background-position: 50%;
  cursor: pointer;
}
.footer__contacts-social:last-child {
  margin-right: 0;
}
.footer__contacts-social--tg {
  background-image: url(/icons/icon__tg.svg);
}
.footer__contacts-social--vk {
  background-image: url(/icons/icon__vk.svg);
}
.footer__contacts-social--fb {
  background-image: url(/icons/icon__fb.svg);
}
.footer__contacts-social--ig {
  background-image: url(/icons/icon__ig.svg);
}
.footer__contacts-contact-us {
  padding: 12px;
  text-align: center;
  font-style: normal;
  font-weight: 600;
  font-size: 12px;
  line-height: 15px;
  letter-spacing: 0.03em;
  text-transform: uppercase;
  color: #000000;
  border: 1px solid #000;
  cursor: pointer;
}
</style>
