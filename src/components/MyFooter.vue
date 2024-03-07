<template>
  <footer>
    <div class="footer_grid container">
      <div>
        <div class="footer_logo">
          <img src="../assets/icons/logo.png" alt="" />
        </div>
        <div class="contacts">
          <h1>Контакты</h1>
          <div class="fd_column gap20">
            <div class="d_flex align_center gap10">
              <span class="icon">
                <img src="../assets/icons/location.svg" alt="" />
              </span>
              <ul>
                <li>г.Ташкент, Чиланзар</li>
                <li>10 квартал, дом 3/1</li>
              </ul>
            </div>
            <div class="d_flex align_center gap10">
              <span class="icon">
                <img src="../assets/icons/call.svg" alt="" />
              </span>
              <ul>
                <li>+998 71 276-62-53</li>
                <li>+998 71 276-62-54</li>
              </ul>
            </div>
          </div>
          <div class="fd_column gap20">
            <div class="d_flex align_center gap10">
              <span class="icon">
                <img src="../assets/icons/location.svg" alt="" />
              </span>
              <ul>
                <li>г.Ташкент, Чиланзар</li>
                <li>10 квартал, дом 3/1</li>
              </ul>
            </div>
            <button class="btn pad10">Оставить заявку</button>
          </div>
        </div>
        <div class="target">
          <div class="footer_logo_no_phone">
            <img src="../assets/icons/logo.png" alt="" />
          </div>
          <p>
            Наша цель – построить прозрачный, долгосрочный бизнес, приносить огромную пользу
            населению, путем решения глобальных вопросов. Внедряя инновационные технологии на рынок
            Узбекистана.
          </p>
        </div>
      </div>
      <div class="footer_tablet d_flex justify_between">
        <div class="footer_links">
          <h1>О компании</h1>
          <a href="">История </a>
          <a href="">Партнеры </a>
          <a href="">Вакансии</a>
        </div>
        <div class="footer_links">
          <h1>Продукция</h1>
          <a href="">Эндоваскулярная хирургия </a>
          <a href=""> Аритмология </a>
          <a href="">Кардиохирургия </a>
          <a href="">Лабораторная диагностика </a>
          <a href="">Хирургия </a>
          <a href="">Эндоурология </a>
          <a href="">Нейрохирургия </a>
          <a href="">Анестезиология и реанимация </a><a href="">Диабет</a>
        </div>
        <div class="footer_links">
          <h1>Услуги</h1>
          <a href="">Сервис </a>
          <a href="">Регистрации </a>
          <a href="">Услуги логистики</a>
        </div>
      </div>
    </div>
    <div class="container">
      <span>© 2021 ООО «Medical Online Services»</span>
      <span class="footer_tablet">Сайт разработан компанией <a href="">www.qodirov.uz</a></span>
    </div>
  </footer>
</template>

<script setup></script>

<style lang="scss" scoped>
@import '../assets/scss/breakpoints';
.contacts {
  display: flex;
  justify-content: space-between;
  gap: 5px;
  @include media('<=phone') {
    flex-direction: column;
    gap: 20px;
    align-items: flex-start;
  }
}
footer {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  background-position: center;
  background-image: url('../assets/fon_img/blur_hospital.svg');
  background-size: cover;
  background-repeat: no-repeat;
  background-color: rgba($color: lightgray, $alpha: 0.5);
  padding: 30px 0;

  .footer_links {
    display: flex;
    flex-direction: column;
  }
  > div {
    display: flex;
    flex-direction: row !important;
    justify-content: space-between;
    > div {
      display: flex;
      flex-direction: column;
      gap: 15px;
      a {
        display: flex;
        color: #595959;
        font-family: Roboto;
        font-size: 16px;
        font-weight: 300;
        &:hover {
          text-decoration: underline;
          color: #00c9c9;
        }
      }
    }
  }
  h1 {
    color: #595959;
    font-family: Roboto;
    font-size: 26px;
    font-weight: 500;
    letter-spacing: 1.04px;
    white-space: nowrap;
  }
}
.target {
  display: flex;
  align-items: center;
  gap: 35px;
  @include media('<=phone') {
    gap: 0;
  }
}
.footer_grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
  @include media('<=tablet') {
    display: flex;
  }
}
.footer_tablet {
  @include media('<=tablet') {
    display: none;
  }
}
.footer_logo {
  display: none;
  justify-content: center;
  img {
    width: 272px;
    height: 79px;
    @include media('<=300px') {
      width: 200px;
      height: 58px;
    }
  }
  @include media('<=phone') {
    display: flex;
  }
}

.footer_logo_no_phone {
  img {
    @include media('<=600px') {
      width: 134px;
      height: 38px;
    }
    @include media('<=phone') {
      display: none;
    }
  }
}
</style>
