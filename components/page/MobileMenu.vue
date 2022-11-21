<template>
  <div class="desktop-hide">
    <div class="mobile-menu">
      <div class="mobile-menu__header">
        <CitySelect :mobile="true"></CitySelect>
        <AuthElement :mobile="true"></AuthElement>
        <div class="mobile-menu__close" @click="closeMenu()"></div>
      </div>
      <div class="mobile-menu__categories">
        <template v-for="(menuItem, menuItemIdx) in menu">
          <div :key="menuItemIdx"
            class="mobile-menu__categories-item"
            :class="{'mobile-menu__categories-item--active': activeCategory === menuItem.name}"
            @click="setActiveCategory(menuItem.name)"
          >{{ menuItem.title }}</div>
        </template>
      </div>
      <div class="mobile-menu__items">
        <template v-if="!activeMenu">
          <template v-for="(subItem, subItemIdx) in menu.find((item) => item.name === activeCategory).items">
            <template v-if="subItem.items && subItem.items.length">
              <div
                :key="subItemIdx"
                class="mobile-menu__items-item"
                @click="setActiveMenu(subItem.name)"
              >
                {{ subItem.title}}
                <span class="mobile-menu__items-item--expand"></span>
              </div>
            </template>
            <template v-else>
              <div
                :key="subItemIdx"
                class="mobile-menu__items-item"
              >
                {{ subItem.title}}
              </div>
            </template>
          </template>
        </template>
        <template v-else>
          <div
            class="mobile-menu__items-item"
            @click="setActiveMenu('')"
          >
            <span class="mobile-menu__items-item--hide"></span>
            {{ menu.find((item) => item.name === activeCategory).items.find((item) => item.name === activeMenu).title }}
          </div>
          <div class="mobile-menu__items-subitems">
            <template v-for="(subSubItem, subSubItemIdx) in menu.find((item) => item.name === activeCategory).items.find((item) => item.name === activeMenu).items">
              <div
                :key="subSubItemIdx"
                class="mobile-menu__items-subitem"
              >
              {{ subSubItem.title }}
              </div>
            </template>
          </div>
        </template>
      </div>
      <div class="mobile-menu__footer">
        <a href="#" class="mobile-menu__footer-item">О нас</a>
        <a href="#" class="mobile-menu__footer-item">Оплата</a>
        <a href="#" class="mobile-menu__footer-item">Доставка</a>
        <a href="#" class="mobile-menu__footer-item">Как заказать</a>
        <a href="#" class="mobile-menu__footer-item">Контакты</a>
        <a href="#" class="mobile-menu__footer-item">Возврат</a>
        <a href="#" class="mobile-menu__footer-item">Публичная оферта</a>
        <a href="#" class="mobile-menu__footer-item">Часто задаваемые вопросы</a>
      </div>
    </div>
  </div>
</template>

<script>
import CitySelect from "@/components/elements/CitySelect";
import BasketElement from "@/components/elements/BasketElement";
import AuthElement from "@/components/elements/AuthElement";

export default {
  components: {
    AuthElement,
    BasketElement,
    CitySelect
  },
  data() {
    return {
      activeCategory: 'men',
      activeMenu: '',
      menu: [
        {
          name: 'men',
          title: 'Мужчинам',
          items: [
            {
              name: 'clothes',
              title: 'Одежда',
              items: [
                {
                  name: 'shirts',
                  title: 'Блузы и рубашки'
                },
                {
                  name: 'body',
                  title: 'Боди'
                },
                {
                  name: 'pants',
                  title: 'Брюки'
                },
                {
                  name: 'outerwear',
                  title: 'Верхняя одежда'
                },
                {
                  name: 'sweatshirt',
                  title: 'Джемперы, свитеры и кардиганы'
                },
                {
                  name: 'jeans',
                  title: 'Джинсы'
                },
                {
                  name: 'homewear',
                  title: 'Домашняя одежда'
                },
                {
                  name: 'beachwear',
                  title: 'Купальники и пляжная одежда'
                },
                {
                  name: 'underwear',
                  title: 'Нижнее белье'
                }
              ]
            },
            {
              name: 'shoes',
              title: 'Обувь',
              items: [
                {
                  name: 'shoes',
                  title: 'Туфли'
                },
                {
                  name: 'sneakers',
                  title: 'Кроссовки'
                },
                {
                  name: 'keds',
                  title: 'Кеды'
                }
              ]
            },
            {
              name: 'accessories',
              title: 'Аксессуары',
              items: [
                {
                  name: 'hats',
                  title: 'Шапки'
                },
                {
                  name: 'gloves',
                  title: 'Перчатки'
                },
                {
                  name: 'bags',
                  title: 'Сумки'
                }
              ]
            },
            {
              name: 'brands',
              title: 'Бренды',
              items: [
                {
                  name: 'gucci',
                  title: 'Gucci'
                },
                {
                  name: 'prada',
                  title: 'Prada'
                },
                {
                  name: 'supreme',
                  title: 'Supreme'
                }
              ]
            },
            {
              name: 'sale',
              title: 'Sale%',
              items: []
            }
          ]
        },
        {
          name: 'women',
          title: 'Женщинам',
          items: [
            {
              name: 'clothes',
              title: 'Одежда',
              items: [
                {
                  name: 'shirts',
                  title: 'Блузы и рубашки'
                },
                {
                  name: 'body',
                  title: 'Боди'
                },
                {
                  name: 'pants',
                  title: 'Брюки'
                },
                {
                  name: 'outerwear',
                  title: 'Верхняя одежда'
                },
                {
                  name: 'sweatshirt',
                  title: 'Джемперы, свитеры и кардиганы'
                },
                {
                  name: 'jeans',
                  title: 'Джинсы'
                },
                {
                  name: 'homewear',
                  title: 'Домашняя одежда'
                },
                {
                  name: 'beachwear',
                  title: 'Купальники и пляжная одежда'
                },
                {
                  name: 'underwear',
                  title: 'Нижнее белье'
                }
              ]
            },
            {
              name: 'shoes',
              title: 'Обувь',
              items: [
                {
                  name: 'shoes',
                  title: 'Туфли'
                },
                {
                  name: 'sneakers',
                  title: 'Кроссовки'
                },
                {
                  name: 'keds',
                  title: 'Кеды'
                }
              ]
            },
            {
              name: 'accessories',
              title: 'Аксессуары',
              items: [
                {
                  name: 'hats',
                  title: 'Шапки'
                },
                {
                  name: 'gloves',
                  title: 'Перчатки'
                },
                {
                  name: 'bags',
                  title: 'Сумки'
                }
              ]
            },
            {
              name: 'brands',
              title: 'Бренды',
              items: [
                {
                  name: 'gucci',
                  title: 'Gucci'
                },
                {
                  name: 'prada',
                  title: 'Prada'
                },
                {
                  name: 'supreme',
                  title: 'Supreme'
                }
              ]
            },
            {
              name: 'sale',
              title: 'Sale%',
              items: []
            }
          ]
        },
        {
          name: 'kid',
          title: 'Детям',
          items: [
            {
              name: 'clothes',
              title: 'Одежда',
              items: [
                {
                  name: 'shirts',
                  title: 'Блузы и рубашки'
                },
                {
                  name: 'body',
                  title: 'Боди'
                },
                {
                  name: 'pants',
                  title: 'Брюки'
                },
                {
                  name: 'outerwear',
                  title: 'Верхняя одежда'
                },
                {
                  name: 'sweatshirt',
                  title: 'Джемперы, свитеры и кардиганы'
                },
                {
                  name: 'jeans',
                  title: 'Джинсы'
                },
                {
                  name: 'homewear',
                  title: 'Домашняя одежда'
                },
                {
                  name: 'beachwear',
                  title: 'Купальники и пляжная одежда'
                },
                {
                  name: 'underwear',
                  title: 'Нижнее белье'
                }
              ]
            },
            {
              name: 'shoes',
              title: 'Обувь',
              items: [
                {
                  name: 'shoes',
                  title: 'Туфли'
                },
                {
                  name: 'sneakers',
                  title: 'Кроссовки'
                },
                {
                  name: 'keds',
                  title: 'Кеды'
                }
              ]
            },
            {
              name: 'accessories',
              title: 'Аксессуары',
              items: [
                {
                  name: 'hats',
                  title: 'Шапки'
                },
                {
                  name: 'gloves',
                  title: 'Перчатки'
                },
                {
                  name: 'bags',
                  title: 'Сумки'
                }
              ]
            },
            {
              name: 'brands',
              title: 'Бренды',
              items: [
                {
                  name: 'gucci',
                  title: 'Gucci'
                },
                {
                  name: 'prada',
                  title: 'Prada'
                },
                {
                  name: 'supreme',
                  title: 'Supreme'
                }
              ]
            },
            {
              name: 'sale',
              title: 'Sale%',
              items: []
            }
          ]
        }
      ]
    }
  },
  methods: {
    setActiveCategory(category) {
      this.activeCategory = category
    },
    setActiveMenu(menu) {
      this.activeMenu = menu
    },
    closeMenu() {
      this.$emit('menu-close')
    }
  }
}
</script>
<style>
@media (min-width: 780px) {
  .desktop-hide {
    display: none;
  }
}
@media (max-width: 780px) {
  .desktop-hide {
    display: block;
  }
}
.mobile-menu {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  overflow: auto;
  background-color: #000;
  z-index: 999;
}
.mobile-menu__header {
  padding:0 18px;
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 44px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: #000;
  z-index: 999;
}
.mobile-menu__close {
  width: 16px;
  height: 16px;
  background-image: url(/icons/icon__menu-close.svg);
  background-repeat: no-repeat;
  background-position: 50%;
  background-size: 30px;
}
.mobile-menu__categories {
  padding:0 18px;
  margin-top: 74px;
  margin-bottom: 38px;
  display: flex;
  justify-content: space-between;
  font-size: 16px;
  font-weight: 600;
  line-height: 20px;
  letter-spacing: 0.03em;
}
.mobile-menu__categories-item {
  color: #C1C1C1;
  position: relative;
}
.mobile-menu__categories-item:hover {
  color: #fff;
}
.mobile-menu__categories-item--active {
  color: #fff;
}
.mobile-menu__items {
  padding:0 18px;
  margin-bottom: 28px;
  font-size: 18px;
  font-weight: 500;
  line-height: 22px;
  letter-spacing: 0;
}
.mobile-menu__items-item {
  margin-bottom: 18px;
  display: flex;
  align-items: center;
  color: #fff;
  text-decoration: none;
}
.mobile-menu__items-subitems {
  margin-top: 32px;
}
.mobile-menu__items-subitem {
  margin-bottom: 12px;
  margin-left: 19px;
  font-size: 16px;
  font-weight: 400;
  line-height: 22px;
  color: #fff;
}
.mobile-menu__items-item--expand {
  margin-left: 12px;
  display: block;
  width: 7px;
  height: 16px;
  background-image: url(/icons/icon__menu-arrow-right.svg);
  background-size: 7px 12px;
  background-repeat: no-repeat;
  background-position: left 0 top 4px;
}
.mobile-menu__items-item--hide {
  margin-right: 12px;
  display: block;
  width: 7px;
  height: 15px;
  background-image: url(/icons/icon__menu-arrow-left.svg);
  background-size: 7px 12px;
  background-repeat: no-repeat;
  background-position: left 0 top 3px;
}
.mobile-menu__footer {
  padding: 28px 18px 44px;
  font-size: 18px;
  font-weight: 500;
  line-height: 22px;
  letter-spacing: 0;
  position: relative;
}
.mobile-menu__footer:before {
  position: absolute;
  top: 0;
  content: "";
  border-top: 1px solid #8E8E8E;
  height: 1px;
  width: calc(100% - 36px);
}
.mobile-menu__footer-item {
  display: block;
  color: #fff;
  text-decoration: none;
  margin-bottom: 18px;
}
</style>
