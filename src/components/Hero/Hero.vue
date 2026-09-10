<template>
  <section class="hero">

    <!-- ========================================
         ЛЕВАЯ КАРТИНКА
         ======================================== -->

    <div class="hero__image">
      <img
        src="../../assets/images/hero/crow.png"
        alt="Рисование"
      >
    </div>


    <!-- ========================================
         ЛОГОТИП
         ======================================== -->

    <div class="hero__branding">
      <img
        src="../../assets/images/hero/big-wings-logo.png"
        alt="Изостудия Big Wings"
      >
    </div>


    <!-- ========================================
         КОНТАКТЫ
         ======================================== -->

    <div class="hero__contacts">

<!-- Социальные сети -->

<div class="hero__socials">

  <a
    href="https://vk.ru/sverhra333um"
    class="hero__social"
    aria-label="MAX"
  >
    <img
      src="../../assets/images/hero/social/max_pict.png"
      alt="MAX"
    >
  </a>


  <a
    href="https://vk.ru/sverhra333um"
    class="hero__social"
    aria-label="VK"
  >
    <img
      src="../../assets/images/hero/social/vk_pict.png"
      alt="VK"
    >
  </a>

</div>




      <!-- Телефон -->
      <a
        href="tel:+79104697054"
        class="hero__phone"
      >
        Тел.: +7 910 460 7054
      </a>


      <!-- Адрес -->

      <address class="hero__address">
        Адрес: Библиотека №3<br>
        Московская область<br>
        г. Мытищи, ул. Силикатная, д. 37<br>
        тел.: +7 910 469 7054<br>
        <span class="hero__second-phone">
          +7 (495) 583 7 34 1
        </span><br>
        mail: lsbigwings@gmail.com<br>
        <span class="hero__second-phone">
          biblioteka_3@mail.ru
        </span><br>
      </address>

    </div>

  </section>
</template>


<style lang="scss" scoped>
@use '../../assets/styles/variables' as *;


/* ========================================
   HERO
   ======================================== */

   .hero {
  display: grid;

  grid-template-columns: repeat(12, minmax(0, 1fr));
  grid-template-rows: 1fr;

  width: 100%;
  height: 800px;
  min-height: 0;

  overflow: hidden;

  background-image: url('../../assets/images/hero/hero-background.png');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}


/* ========================================
   IMAGE
   ======================================== */
   .hero__image {
  grid-column: 1 / 5;
  grid-row: 1;

  align-self: start;
  justify-self: start;

  z-index: 1;

  width: 100%;
  height: 100%;

  min-width: 0;
  min-height: 0;

  display: flex;
  align-items: flex-start;
  justify-content: flex-start;

  overflow: visible;
}


.hero__image img {
  display: block;

  height: 140%;
  width: auto;

  max-width: none;
  flex-shrink: 0;

  /*
   * Смещение отдельно от масштаба.
   */
  transform: translateX(-45%);
}

/* ========================================
   LOGO
   ======================================== */

.hero__branding {
  grid-column: 5 / 9;
  grid-row: 1;

  align-self: center;
  justify-self: center;

  z-index: 2;

  display: flex;
  align-items: center;
  justify-content: center;

  width: 100%;
}

.hero__branding img {
  display: block;

  width: min(100%, 420px);
  height: auto;
}


/* ========================================
   CONTACTS
   ======================================== */

.hero__contacts {
  grid-column: 9 / 13;
  grid-row: 1;

  align-self: center;
  justify-self: center;

  z-index: 3;

  display: flex;
  flex-direction: column;
  align-items: flex-start;

  text-align: left;
}


/* ========================================
   SOCIALS
   ======================================== */

.hero__socials {
  display: flex;
  align-items: center;
  align-self: center;
  gap: 14px;

  margin-bottom: 24px;
}

.hero__social {
  display: flex;
  align-items: center;
  justify-content: center;

  width: 40px;
  height: 40px;
}

.hero__social img {
  display: block;

  width: 100%;
  height: 100%;

  object-fit: contain;
}


/* ========================================
   PHONE
   ======================================== */

.hero__phone {
  display: block;

  font-size: 24px;
  font-weight: 600;

  color: $color-black;

  text-decoration: none;

  transition: opacity $transition-fast;

  &:hover {
    opacity: 0.6;
  }
}


/* ========================================
   ADDRESS
   ======================================== */

.hero__address {
  margin-top: 14px;

  font-size: 18px;
  line-height: 1.4;

  font-style: normal;

  text-align: left;
}


/*
 * Второй телефон выступает вправо
 * относительно остального текста.
 */

.hero__second-phone {
  display: inline-block;

  margin-left: 44px;
}


/* ========================================
   TABLET
   ======================================== */

@media (max-width: 1000px) {

  .hero {
    grid-template-columns: repeat(8, 1fr);
  }


  .hero__image {
    grid-column: 1 / 4;
  }


  .hero__branding {
    grid-column: 3 / 7;
  }


  .hero__branding img {
    width: min(100%, 320px);
  }


  .hero__contacts {
    grid-column: 6 / 9;
  }


  .hero__social {
    width: 32px;
    height: 32px;
  }


  .hero__phone {
    font-size: 20px;
  }


  .hero__address {
    font-size: 16px;
  }
}


/* ========================================
   MOBILE
   ======================================== */
   @media (max-width: 600px) {
    .hero {
  position: relative;

  grid-template-columns: 1fr;
  grid-template-rows: auto auto;

  height: auto;
  min-height: 0;

  /*
   * Небольшой зазор после контактов.
   */
  padding-bottom: 12px;

  overflow: hidden;

  box-sizing: border-box;
}


/* ========================================
   ЛОГОТИП
   ======================================== */
.hero__branding {
  grid-column: 1;
  grid-row: 1;

  align-self: start;
  justify-self: center;

  width: 100%;

  margin-top: 40px;
}


.hero__branding img {
  display: block;

  width: min(80%, 300px);
  height: auto;

  margin: 0 auto;
}


/* ========================================
   КАРТИНКА
   ======================================== */
   .hero__image {
  grid-column: 1;
  grid-row: 2;

  align-self: start;
  justify-self: start;

  width: 100%;
  height: 0;

  min-width: 0;
  min-height: 0;

  display: flex;
  align-items: flex-start;
  justify-content: flex-start;

  overflow: visible;

  z-index: 1;

  pointer-events: none;
}

.hero__image img {
  display: block;

  width: 300%;
  height: auto;

  max-width: none;
  flex-shrink: 0;

  transform: translateX(-50%);
}

/* ========================================
   КОНТАКТЫ
   ======================================== */
   .hero__contacts {
  grid-column: 1;
  grid-row: 2;

  align-self: start;
  justify-self: center;

  width: 100%;

  margin-top: 320px;
  margin-left: 40px;

  display: flex;
  flex-direction: column;
  align-items: center;

  text-align: center;

  z-index: 3;
}

/* ========================================
   СОЦИАЛЬНЫЕ СЕТИ
   ======================================== */

.hero__socials {
  
  gap: 8px;

  margin-bottom: 12px;
  margin-left: 100px;
}


.hero__social {
  width: 28px;
  height: 28px;
}


/* ========================================
   ТЕЛЕФОН
   ======================================== */

.hero__phone {
  font-size: 16px;
}


/* ========================================
   АДРЕС
   ======================================== */

.hero__address {
  margin-top: 10px;

  font-size: 13px;
  line-height: 1.4;

  text-align: center;
}


.hero__second-phone {
  margin-left: 0;
}

}
</style>