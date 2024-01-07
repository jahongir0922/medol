<template>
  <div id="header">
    <div class="header_top">
      <div class="d_flex gap10">
        <div class="adress d_flex align_center gap10">
          <span class="icon">
            <img src="../assets/icons/location.svg" alt="" />
          </span>
          <ul>
            <li>г.Ташкент, Чиланзар</li>
            <li>10 квартал, дом 3/1</li>
          </ul>
        </div>
        <div class="numbers d_flex align_center gap10">
          <span class="icon">
            <img src="../assets/icons/call.svg" alt="" />
          </span>
          <ul>
            <li>+998 71 276-62-53</li>
            <li>+998 71 276-62-54</li>
          </ul>
        </div>
      </div>
      <div class="logo align_center">
        <img src="../assets/icons/logo.png" alt="" />
      </div>
      <div class="d_flex align_center justify_end gap10">
        <span class="on_tablet location icon">
          <img src="../assets/icons/location.svg" alt="" />
        </span>
        <span class="on_tablet icon">
          <img src="../assets/icons/call.svg" alt="" />
        </span>
        <span id="search" @click="serch_on()" ref="search" class="icon search">
          <img src="../assets/icons/search.svg" alt="" />
        </span>
        <span id="search_span" ref="search_span" class="search_span">
          <input
            id="search_input"
            v-model="search_input"
            placeholder="Поиск по сайту"
            type="text"
          />
        </span>
        <a href="#" class="facebook">
          <img src="../assets/icons/facebook.svg" alt="" />
          Мы на Facebook
        </a>
        <div class="drop_down_lang">
          <span lang_span="en" class="lang">
            <img class="flag" src="../assets/icons/flag_en.svg" alt="" />
            <span>English</span></span
          >
          <span lang_span="uz" class="lang">
            <img class="flag" src="../assets/icons/flag_uz.svg" alt="" />
            <span>O'zbekcha</span></span
          >
          <span lang_span="ru" class="lang lang_active">
            <img class="flag" src="../assets/icons/flag_ru.svg" alt="" />
            <span>Русский</span></span
          >
          <img src="../assets/icons/arrow_down.svg" alt="" />
          <div class="select_lang">
            <a @click="changelang('en')" href="#en">
              <img class="flag" src="../assets/icons/flag_en.svg" alt="" />
              English</a
            >
            <a @click="changelang('uz')" href="#uz">
              <img class="flag" src="../assets/icons/flag_uz.svg" alt="" />
              O'zbekcha</a
            >
            <a @click="changelang('ru')" href="#ru">
              <img class="flag" src="../assets/icons/flag_ru.svg" alt="" />
              Русский</a
            >
          </div>
        </div>
        <span id="search" @click="" ref="" class="icon menu">
          <img src="../assets/icons/menu.svg" alt="" />
          <div class="nav_links_on_tablet">
            <RouterLink to="/home">МАГАЗИН</RouterLink>
            <RouterLink to="/about">О КОМПАНИИ</RouterLink>
            <RouterLink to="/dfs">ПРОДУКЦИЯ</RouterLink>
            <RouterLink to="/dsd">УСЛУГИ</RouterLink>
            <RouterLink to="/dfxdz">АКЦИИ И НОВОСТИ</RouterLink>
            <RouterLink to="/gdfdz">ОБРАТНАЯ СВЯЗЬ</RouterLink>
            <a href="#" class="menu_facebook">
              <img src="../assets/icons/facebook.svg" alt="" />
              Мы на Facebook
            </a>
            <RouterLink to="/">Выход</RouterLink>
          </div>
        </span>
        <RouterLink class="exit" to="/">Выход</RouterLink>
      </div>
    </div>
    <div class="nav_links">
      <RouterLink data-i18n-en="MARKET" data-i18n-uz="MAGAZIN" data-i18n-ru="МАГАЗИН" to="/home"
        >МАГАЗИН</RouterLink
      >
      <RouterLink
        data-i18n-en="ABOUT US"
        data-i18n-uz="KOMPANIYA HAQIDA"
        data-i18n-ru="О КОМПАНИИ"
        to="/about"
        >О КОМПАНИИ</RouterLink
      >
      <RouterLink
        data-i18n-en="PRODUCTS"
        data-i18n-uz="MAHSULOTLAR"
        data-i18n-ru="ПРОДУКЦИЯ"
        to="/home2"
        >ПРОДУКЦИЯ</RouterLink
      >
      <RouterLink data-i18n-en="SERVICES" data-i18n-uz="XIZMATLAR" data-i18n-ru="УСЛУГИ" to="/home3"
        >УСЛУГИ</RouterLink
      >
      <RouterLink
        data-i18n-en="PROMOTION"
        data-i18n-uz="AKSIYA VA YANGILIKLAR"
        data-i18n-ru="АКЦИИ И НОВОСТИ"
        to="/home4"
        >АКЦИИ И НОВОСТИ</RouterLink
      >
      <RouterLink
        data-i18n-en="FEEDBACK"
        data-i18n-uz="ALOQA"
        data-i18n-ru="ОБРАТНАЯ СВЯЗЬ"
        to="/home5"
        >ОБРАТНАЯ СВЯЗЬ</RouterLink
      >
    </div>
  </div>
</template>

<script setup>
import { onMounted, ref } from 'vue'
const lang = document.documentElement.lang
const search = ref(null)
const search_span = ref(null)
const search_input = ref('')
function serch_on() {
  search.value.style.display = 'none'
  search_span.value.style.display = 'flex'
  let search_input = document.querySelector('#search_input')
  search_input.style.display = 'block'
}
function serch_off() {
  search.value.style.display = 'flex'
  search_span.value.style.display = 'none'
}
function changelang(lang) {
  ///toggle active class
  let lang_span = document.querySelector(`[lang_span="${lang}"]`)
  let drop_down_lang = document.querySelector('.drop_down_lang')
  drop_down_lang.querySelector('.lang_active').classList.remove('lang_active')
  let select_lang = document.querySelector('.select_lang')
  select_lang.style.display = 'none'
  lang_span.classList.add('lang_active')
  ///toggle active class
  document.documentElement.lang = lang
  let elements = document.documentElement.getElementsByTagName('*')
  for (var i = 0; i < elements.length; i++) {
    if (elements[i].getAttribute('data-i18n-' + lang)) {
      elements[i].innerHTML = elements[i].getAttribute('data-i18n-' + lang)
    }
  }
}
window.addEventListener('click', (event) => {
  let search_span = document.getElementById('search_span')
  let search = document.getElementById('search')
  let img = search.querySelector('img')
  let search_input = document.getElementById('search_input')
  if (
    event.target != search_span &&
    event.target != search &&
    event.target != search_input &&
    event.target != img
  ) {
    serch_off()
  }
})
onMounted(() => {
  let drop_down_lang = document.querySelector('.drop_down_lang')
  drop_down_lang.addEventListener('mouseover', (element) => {
    let select_lang = document.querySelector('.select_lang')
    select_lang.style.display = 'flex'
  })
  drop_down_lang.addEventListener('mouseout', (element) => {
    let select_lang = document.querySelector('.select_lang')
    select_lang.style.display = 'none'
  })
  if (window.location.hash) {
    changelang(window.location.hash.slice(1))
  }
})
</script>

<style lang="scss" scoped>
@import '../assets/scss/breakpoints';
#header {
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 10px;
}
.header_top {
  display: flex;
  justify-content: space-between;
}
.on_tablet {
  display: none;
  position: relative;
  @include media('<=768px') {
    display: flex;
  }
}
.menu {
  display: none;
  @include media('<=768px') {
    display: flex;
  }
  &:hover .nav_links_on_tablet {
    display: flex;
  }
  .nav_links_on_tablet {
    position: absolute;
    display: none;
    flex-direction: column;
    flex-wrap: nowrap;
    align-items: flex-start;
    top: 110%;
    right: 10px;
    gap: 10px;
    padding: 10px;
    z-index: 9;
    border-radius: 10px;
    background-color: white;
    a {
      color: $text_blue;
      font-size: 18px;
      white-space: nowrap;
    }
    .menu_facebook {
      display: flex;
      align-items: center;
      justify-content: flex-start;
      background-color: white;
      border-radius: 25px;
      img {
        width: 25px;
        height: 20px;
      }
    }
  }
}
.search {
  @include media('<=700px') {
    display: none !important;
  }
}
.location {
  @include media('<=600px') {
    display: none;
  }
}
@keyframes search_anim {
  from {
    width: 50px;
  }
  to {
    width: 100%;
  }
}
.search_span {
  display: none;
  align-items: center;
  justify-content: center;
  height: 50px;
  background-color: white;
  border-radius: 25px;
  position: relative;
  padding-right: 10px;
  animation-name: search_anim;
  animation-duration: 1s;
  animation-timing-function: ease-in-out;
  &::before {
    content: '';
    width: 50px;
    height: 50px;
    border-radius: 25px;
    z-index: 10;
    background-image: url(../assets/icons/search_input.svg);
    background-repeat: no-repeat;
    background-position: center;
    background-color: #0d4c93;
  }
  input {
    display: none;
    padding: 5px;
    border: none;
    outline: none;
    animation-name: search_anim;
    animation-duration: 1s;
    animation-timing-function: ease-in;
    &:focus {
      border: none;
    }
  }
}
.numbers,
.adress {
  @include media('<=768px') {
    display: none;
  }
}
.facebook {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 50px;
  padding: 10px;
  background-color: white;
  border-radius: 25px;
  white-space: nowrap;
  @include media('<=768px') {
    display: none;
  }
  &:hover {
    img {
      filter: brightness(0) saturate(100%) invert(59%) sepia(62%) saturate(2447%) hue-rotate(138deg)
        brightness(99%) contrast(100%);
    }
  }
  img {
    width: 25px;
    height: 20px;
  }
}
.drop_down_lang {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 50px;
  padding: 10px;
  gap: 5px;
  background-color: white;
  border-radius: 25px;
  @include media('<=600px') {
    height: 40px;
    border-radius: 20px;
  }
  .flag {
    width: 25px;
    height: 25px;
    border-radius: 50%;
    box-shadow: 0 0 2px black;
  }
}
.exit {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 50px;
  padding: 10px;
  gap: 5px;
  background-color: white;
  border-radius: 25px;
  @include media('<=600px') {
    display: none;
  }
}
.select_lang {
  position: absolute;
  display: none;
  flex-direction: column;
  top: 100%;
  right: 0;
  background-color: white;
  z-index: 5;
  border-radius: 15px;
  box-shadow: 0px 1px 4px 0px rgba(13, 76, 147, 0.1);
  overflow: hidden;
  padding: 10px 0;
  > a {
    display: flex;
    padding: 10px;
    align-items: center;
    gap: 5px;
    &:hover {
      background-color: #ecf5f5;
    }
  }
}
.lang {
  display: none;
  align-items: center;
  gap: 5px;
  span {
    @include media('<=768px') {
      display: none;
    }
  }
}
.lang_active {
  display: flex;
}
.nav_links {
  display: flex;
  gap: 2px;
  @include media('<=768px') {
    display: none;
  }
  :first-child {
    border-top-left-radius: 35px;
    border-bottom-left-radius: 35px;
  }
  :last-child {
    border-top-right-radius: 35px;
    border-bottom-right-radius: 35px;
  }
  > a {
    display: flex;
    align-items: center;
    flex: 1 1 auto;
    justify-content: center;
    padding: 25px;
    color: $text_blue;
    font-size: 20px;
    background-color: white;
    white-space: nowrap;
    @include media('<=desktop') {
      font-size: 16px;
      padding: 15px;
    }
    @include media('<=850px') {
      font-size: 14px;
      padding: 15px;
    }

    &:hover {
      color: $text_blue_active;
      position: relative;
      &::before {
        content: '';
        position: absolute;
        top: 10px;
        right: 10px;
        width: 12px;
        height: 12px;
        border-radius: 50%;
        background-color: $text_blue_active;
        @include media('<=desktop') {
          top: 5px;
          right: 5px;
        }
      }
    }
  }
  .router-link-exact-active {
    color: $text_blue_active;
    position: relative;
    &::before {
      content: '';
      position: absolute;
      top: 10px;
      right: 10px;
      width: 12px;
      height: 12px;
      border-radius: 50%;
      background-color: $text_blue_active;
      @include media('<=desktop') {
        top: 5px;
        right: 5px;
      }
    }
  }
}
</style>
