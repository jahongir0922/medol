<template>
  <div class="home">
    <section class="home_section1">
      <div class="container">
        <MyHeader />
      </div>
      <swiper
        :slidesPerView="1"
        :rewind="true"
        :spaceBetween="40"
        :modules="modules"
        :pagination="{
          clickable: true
        }"
        class="mySwiper"
      >
        <swiper-slide>
          <div class="container main_slide">
            <div class="align_start justify_center gap30 fd_column">
              <h1 class="sarlavha">Анализатор ABL800 FLEX</h1>
              <p>
                Ориентированный на среднюю или высокую производительность тестов, анализатор ABL800
                FLEX измеряет полный набор параметров, включая pH, газы крови, электролиты,
                метаболиты и показатели оксиметрии
              </p>
              <button class="btn">Подробнее</button>
            </div>
            <div class="main_slide_img">
              <img src="../assets/fon_img/ellipse.svg" alt="" />
              <img src="../assets/img/flex.svg" alt="" />
            </div>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="container main_slide">
            <div class="align_start justify_center gap30 fd_column">
              <h1 class="sarlavha">Аппарат ИК-лазерный МАКДЭЛ-09.1</h1>
              <p>
                Ориентированный на среднюю или высокую производительность тестов, анализатор ABL800
                FLEX измеряет полный набор параметров, включая pH, газы крови, электролиты,
                метаболиты и показатели оксиметрии
              </p>
              <button class="btn">Подробнее</button>
            </div>
            <div class="main_slide_img">
              <img src="../assets/fon_img/ellipse.svg" alt="" />
              <img src="../assets/img/makdel.svg" alt="" />
            </div>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="container main_slide">
            <div class="align_start justify_center gap30 fd_column">
              <h1 class="sarlavha">Глюкометр для измерения глюкозы</h1>
              <p>
                Ориентированный на среднюю или высокую производительность тестов, анализатор ABL800
                FLEX измеряет полный набор параметров, включая pH, газы крови, электролиты,
                метаболиты и показатели оксиметрии
              </p>
              <button class="btn">Подробнее</button>
            </div>
            <div class="main_slide_img">
              <img src="../assets/fon_img/ellipse.svg" alt="" />
              <img src="../assets/img/glukometr.svg" alt="" />
            </div>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="container main_slide">
            <div class="align_start justify_center gap30 fd_column">
              <h1 class="sarlavha">Система для аутогемотрансфузии</h1>
              <p>
                Ориентированный на среднюю или высокую производительность тестов, анализатор ABL800
                FLEX измеряет полный набор параметров, включая pH, газы крови, электролиты,
                метаболиты и показатели оксиметрии
              </p>
              <button class="btn">Подробнее</button>
            </div>
            <div class="main_slide_img">
              <img src="../assets/fon_img/ellipse.svg" alt="" />
              <img src="../assets/img/gematransfuzi.svg" alt="" />
            </div>
          </div>
        </swiper-slide>
      </swiper>
    </section>
    <section class="container home_section2">
      <h1 class="sarlavha">ПРОДУКЦИЯ</h1>
      <div class="pruducts">
        <div class="product_card">
          <img src="../assets/img/endeavor.png" alt="" />
          <p>Эндоваскулярная хирургия</p>
          <button class="btn">Посмотреть все</button>
        </div>
        <div class="product_card">
          <img src="../assets/img/lab_diag.png" alt="" />
          <p>Лабораторная диагностика</p>
          <button class="btn">Посмотреть все</button>
        </div>
        <div class="product_card">
          <img src="../assets/img/kardio_xirurg.png" alt="" />
          <p>Кардиохирургия</p>
          <button class="btn">Посмотреть все</button>
        </div>
        <div class="product_card">
          <img src="../assets/img/diabet.png" alt="" />
          <p>ДИАБЕТ</p>
          <button class="btn">Посмотреть все</button>
        </div>
        <div class="product_card">
          <img src="../assets/img/endo_uro.png" alt="" />
          <p>ЭНДОУРОЛОГИЯ</p>
          <button class="btn">Посмотреть все</button>
        </div>
        <div class="product_card">
          <img src="../assets/img/aritmologiya.png" alt="" />
          <p>АРИТМОЛОГИЯ</p>
          <button class="btn">Посмотреть все</button>
        </div>
      </div>
      <a class="link" href="/">
        Перейти в каталог нашей продукции ><img src="../assets/icons/right_arrow.svg" alt="" />
      </a>
    </section>
    <section class="home_section3">
      <h1 class="sarlavha">УСЛУГИ</h1>
      <div class="service_bg">
        <div class="container">
          <swiper
            :slidesPerView="3"
            :rewind="true"
            :spaceBetween="40"
            :modules="modules"
            :pagination="{
              clickable: true
            }"
            :breakpoints="swiperOptions3.breakpoints"
            class="mySwiper service container"
          >
            <swiper-slide>
              <div class="card">
                <img src="../assets/img/service1.png" alt="" />
                <div>
                  <h1>СЕРВИС ОБОРУДОВАНИЯ</h1>
                  <p>
                    Компания предоставляет сервисное обслуживание по всем предоставляемым продуктам.
                    У наших инженеров имеется опыт и сертификаты фирм производителей......
                  </p>
                </div>
                <button class="btn">Подробнее</button>
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="card">
                <img src="../assets/img/service2.png" alt="" />
                <div>
                  <h1>РЕГИСТРАЦИИ</h1>
                  <p>
                    Обеспечение получения разрешительных документов, регистрационного удостоверения
                    на изделия медицинского назначения Подготовка объектов к проведению ....
                  </p>
                </div>
                <button class="btn">Подробнее</button>
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="card">
                <img src="../assets/img/service3.png" alt="" />
                <div>
                  <h1>УСЛУГИ ЛОГИСТИКИ</h1>
                  <p>
                    Компания предоставляет сервисное обслуживание по всем предоставляемым продуктам.
                    У наших инженеров имеется опыт и сертификаты фирм производителей.....
                  </p>
                </div>
                <button class="btn">Подробнее</button>
              </div>
            </swiper-slide>
          </swiper>
        </div>
      </div>
    </section>
    <section class="container home_section4">
      <h1 class="sarlavha">О КОМПАНИИ</h1>
      <div class="about_company">
        <img src="../assets/icons/logo_about.svg" alt="" />
        <div>
          <p>
            Группа компаний MEDOL создавалась высококвалифицированными специалистами в сфере
            медицины, инженерии и экономики, за плечами которых значительный опыт на рынке высоких
            медицинских технологий, которая имеет свои представительства в разных уголках Земли. В
            2011 году MEDOL зарегистрировал в Узбекистане ИП ООО “Medical Online Services". Цель
            компании построить прозрачный долгосрочный бизнес, принести пользу обществу путем
            развития и внедрения передовых технологий в систему здравоохранения Республики
            Узбекистан.
          </p>
          <button class="btn">Узнать больше</button>
        </div>
      </div>
    </section>
    <section class="container home_section5">
      <h1 class="sarlavha">НОВОСТИ</h1>
      <swiper
        :loop="true"
        :spaceBetween="30"
        :modules="modules"
        :slidesPerView="3"
        :navigation="true"
        class="mySwiper news"
        :breakpoints="swiperOptions3.breakpoints"
      >
        <swiper-slide>
          <div class="card_news">
            <img src="../assets/img/news1.png" alt="" />
            <div>
              <h1>Mастер-класс в исполнении Галлямова Эдуарда Абдулхаевича</h1>
              <h1>26.07.2021</h1>
              <p>
                С 19 по 21 апреля в АО «РСНПМЦУ» (Республиканский Специализированный
                Научно-Практический Медицинский Центр Урологии) при поддержке компаний Ethicon Endo
                Surgery (Johnson&Johnson) и ИП ООО «Medical Online Services» был проведен
                мастер-класс в исполнении...
              </p>
            </div>
            <button class="btn">Подробнее</button>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="card_news">
            <img src="../assets/img/news1.png" alt="" />
            <div>
              <h1>Mастер-класс в исполнении Галлямова Эдуарда Абдулхаевича</h1>
              <h1>26.07.2021</h1>
              <p>
                С 19 по 21 апреля в АО «РСНПМЦУ» (Республиканский Специализированный
                Научно-Практический Медицинский Центр Урологии) при поддержке компаний Ethicon Endo
                Surgery (Johnson&Johnson) и ИП ООО «Medical Online Services» был проведен
                мастер-класс в исполнении...
              </p>
            </div>
            <button class="btn">Подробнее</button>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="card_news">
            <img src="../assets/img/news1.png" alt="" />
            <div>
              <h1>Mастер-класс в исполнении Галлямова Эдуарда Абдулхаевича</h1>
              <h1>26.07.2021</h1>
              <p>
                С 19 по 21 апреля в АО «РСНПМЦУ» (Республиканский Специализированный
                Научно-Практический Медицинский Центр Урологии) при поддержке компаний Ethicon Endo
                Surgery (Johnson&Johnson) и ИП ООО «Medical Online Services» был проведен
                мастер-класс в исполнении...
              </p>
            </div>
            <button class="btn">Подробнее</button>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="card_news">
            <img src="../assets/img/news1.png" alt="" />
            <div>
              <h1>Mастер-класс в исполнении Галлямова Эдуарда Абдулхаевича</h1>
              <h1>26.07.2021</h1>
              <p>
                С 19 по 21 апреля в АО «РСНПМЦУ» (Республиканский Специализированный
                Научно-Практический Медицинский Центр Урологии) при поддержке компаний Ethicon Endo
                Surgery (Johnson&Johnson) и ИП ООО «Medical Online Services» был проведен
                мастер-класс в исполнении...
              </p>
            </div>
            <button class="btn">Подробнее</button>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="card_news">
            <img src="../assets/img/news1.png" alt="" />
            <div>
              <h1>Mастер-класс в исполнении Галлямова Эдуарда Абдулхаевича</h1>
              <h1>26.07.2021</h1>
              <p>
                С 19 по 21 апреля в АО «РСНПМЦУ» (Республиканский Специализированный
                Научно-Практический Медицинский Центр Урологии) при поддержке компаний Ethicon Endo
                Surgery (Johnson&Johnson) и ИП ООО «Medical Online Services» был проведен
                мастер-класс в исполнении...
              </p>
            </div>
            <button class="btn">Подробнее</button>
          </div>
        </swiper-slide>
      </swiper>
      <div class="links">
        <a class="link" href="/">
          Посмотреть все новости ><img src="../assets/icons/right_arrow.svg" alt="" />
        </a>
        <a class="link" href="/">
          Подписаться на новости ><img src="../assets/icons/right_arrow.svg" alt="" />
        </a>
      </div>
    </section>
    <section class="container home_section6">
      <h1 class="sarlavha">ПАРТНЕРЫ</h1>
      <swiper
        :slidesPerView="4"
        :grid="{
          rows: 2
        }"
        :rewind="true"
        :spaceBetween="40"
        :navigation="true"
        :modules="modules"
        class="mySwiper partners"
        @swiper="set_swiper_partners"
        @slide-change="update_swiper_partners_Index"
        :breakpoints="swiperOptions.breakpoints"
      >
        <swiper-slide>
          <div class="partner_card">
            <img src="../assets/img/partner1.png" alt="" /></div
        ></swiper-slide>
        <swiper-slide>
          <div class="partner_card">
            <img src="../assets/img/partner2.png" alt="" /></div
        ></swiper-slide>
        <swiper-slide>
          <div class="partner_card">
            <img src="../assets/img/partner3.png" alt="" /></div
        ></swiper-slide>
        <swiper-slide>
          <div class="partner_card">
            <img src="../assets/img/partner4.png" alt="" /></div
        ></swiper-slide>
        <swiper-slide>
          <div class="partner_card">
            <img src="../assets/img/partner5.png" alt="" /></div
        ></swiper-slide>
        <swiper-slide>
          <div class="partner_card">
            <img src="../assets/img/partner6.png" alt="" /></div
        ></swiper-slide>
        <swiper-slide>
          <div class="partner_card">
            <img src="../assets/img/partner7.png" alt="" /></div
        ></swiper-slide>
        <swiper-slide>
          <div class="partner_card">
            <img src="../assets/img/partner8.png" alt="" /></div
        ></swiper-slide>
        <swiper-slide>
          <div class="partner_card">
            <img src="../assets/img/partner1.png" alt="" /></div
        ></swiper-slide>
        <div
          :disabled="swiper_partner_index === 0"
          @click="prev_partners"
          class="swiper-button-prev"
        ></div>
        <div
          :disabled="swiper_partner_index === 1"
          @click="next_partners"
          class="swiper-button-next"
        ></div>
      </swiper>
    </section>
    <MyFooter />
  </div>
</template>
<script setup lang="js">
import { ref } from 'vue'
import MyHeader from '../components/MyHeader.vue'
import MyFooter from '../components/MyFooter.vue'
import { Swiper, SwiperSlide } from 'swiper/vue'
import { Grid, Pagination, Navigation } from 'swiper/modules'
import 'swiper/css'
import 'swiper/css/grid'
import 'swiper/css/navigation'
import 'swiper/css/pagination'
import '../assets/scss/swiper.css'

// with custom button and custom function
let swiper_partners = ref(null)
const set_swiper_partners = (swiper) => {
  swiper_partners = swiper
}
const swiper_partner_index = ref(null)
const update_swiper_partners_Index = () => {
  swiper_partner_index.value = swiper_partners?.activeIndex
}
const prev_partners = () => swiper_partners?.slidePrev()
const next_partners = () => swiper_partners?.slideNext()
// with custom button and custom function
const modules = [Grid, Pagination, Navigation]

const swiperOptions3 = {
  breakpoints: {
    0: {
      slidesPerView: 1,
      spaceBetween: 5
    },
    650: {
      slidesPerView: 2,
      spaceBetween: 20
    },
    1025: {
      slidesPerView: 3,
      spaceBetween: 30
    }
  }
}
const swiperOptions = {
  breakpoints: {
    0: {
      slidesPerView: 1,
      spaceBetween: 5
    },
    650: {
      slidesPerView: 2,
      spaceBetween: 20
    },
    1025: {
      slidesPerView: 3,
      spaceBetween: 30
    },
    1366: {
      slidesPerView: 4,
      spaceBetween: 30
    }
  }
}
</script>

<style lang="scss" scoped></style>
