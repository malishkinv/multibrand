<template>
  <div>
    <div class="d-flex align-items-center mainmenu">
      <template v-for="(item, itemIdx) in menu">
        <div
          :key="itemIdx"
          class="mainmenu__item"
          :class="{
            'mobile-hide': !item.mobile,
            'mainmenu__item--active': item.name === menuActive
          }"
          @mouseover="menuActive = item.name"
        >{{ item.title }}</div>
      </template>
    </div>
    <div v-if="menuActive" class="mainmenu-items mobile-hide" @mouseleave="menuActive = ''">
      <div class="mainmenu-items__wrapper">
        <div class="row">
          <div class="col-9">
            <div class="mainmenu-items__items">
              <template v-for="(subItem, subItemIdx) in menu.find((item) => item.name === menuActive).items">
                <a :key="subItemIdx" href="#" class="mainmenu-items__item">{{ subItem.title }}</a>
              </template>
            </div>
          </div>
          <div class="col-3">
            <img src="/menu-ad.png" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      menuActive: '',
      menu: [
        {
          name: 'clothes',
          title: 'Одежда',
          mobile: false,
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
            },
            {
              name: 'underwear',
              title: 'Носки, чулки и колготки'
            },
            {
              name: 'bigsize',
              title: 'Одежда больших размеров'
            },
            {
              name: 'pregnant',
              title: 'Одежда для беременных'
            },
            {
              name: 'blazers',
              title: 'Пидкажи и костюмы'
            },
            {
              name: 'dress',
              title: 'Платья и сарафаны'
            },
            {
              name: 'sportswear',
              title: 'Спортивные костюмы'
            },
            {
              name: 'tops',
              title: 'Топы и майки'
            },
            {
              name: 'tunicas',
              title: 'Туники'
            },
            {
              name: 'tshirts',
              title: 'Футболки и поло'
            },
            {
              name: 'hoodies',
              title: 'Худи и свитшоты'
            },
            {
              name: 'shorts',
              title: 'Шорты'
            },
            {
              name: 'skirts',
              title: 'Юбки'
            }
          ]
        },
        {
          name: 'shoes',
          title: 'Обувь',
          mobile: false,
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
          mobile: false,
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
          mobile: false,
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
          mobile: false,
          items: []
        }
      ]
    }
  }
}
</script>
<style>
.mainmenu {
  color: #000000;
  margin: 0 auto;
  justify-content: center;
}
.mainmenu__item {
  padding: 15px 30px;
  width: fit-content;
  text-align: center;
  font-style: normal;
  font-weight: 500;
  font-size: 18px;
  line-height: 22px;
  cursor: pointer;
  transition: all .1s;
}
.mainmenu__item:hover {
  background-color: #000;
  color: #fff;
}
.mainmenu__item--active {
  background-color: #000;
  color: #fff;
}
.mainmenu__item:last-child {
  margin-right: 0;
}
.mainmenu-items {
  position: absolute;
  z-index: 999;
  width: 100vw;
  max-height: 370px;
  margin-left: calc(0px - ((100vw - 1280px) / 2));
  background-color: #000;
}
.mainmenu-items__wrapper {
  max-width: 1280px;
  padding: 40px 0;
  margin: 0 auto;
}
.mainmenu-items__items {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 10px;
}
.mainmenu-items__item {
  color: #fff;
  transition: color .2s;
  display: block;
  text-decoration: none;
}
.mainmenu-items__item:hover {
  color: #8E8E8E;
  text-decoration: none;
}
@media (max-width: 780px) {
  .mobile-hide {
    display: none;
  }
  .mainmenu {
    justify-content: space-between;
    padding: 0 18px;
  }
  .mainmenu__item {
    font-size: 16px;
    margin-right: 0;
    line-height: 20px;
    text-transform: uppercase;
  }
}
</style>
