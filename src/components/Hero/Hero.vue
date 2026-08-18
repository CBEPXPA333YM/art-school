<template>
  <section class="hero">

    <!-- ========================================
         ЛЕВАЯ КАРТИНКА
         ======================================== -->

    <div class="hero__image">
      <img
        src="../../assets/images/hero/hero-image.png"
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
          href="#"
          class="hero__social"
          aria-label="VK"
        >
          <img
            src="../../assets/images/hero/social/vk.png"
            alt="VK"
          >
        </a>

        <a
          href="#"
          class="hero__social"
          aria-label="Instagram"
        >
          <img
            src="../../assets/images/hero/social/instagram.png"
            alt="Instagram"
          >
        </a>

        <a
          href="#"
          class="hero__social"
          aria-label="Facebook"
        >
          <img
            src="../../assets/images/hero/social/facebook.png"
            alt="Facebook"
          >
        </a>

        <a
          href="#"
          class="hero__social"
          aria-label="WhatsApp"
        >
          <img
            src="../../assets/images/hero/social/whatsapp.png"
            alt="WhatsApp"
          >
        </a>

        <a
          href="#"
          class="hero__social"
          aria-label="Telegram"
        >
          <img
            src="../../assets/images/hero/social/telegram.png"
            alt="Telegram"
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

  grid-template-columns: repeat(12, 1fr);
  grid-template-rows: 1fr;

  width: 100%;

  /*
   * Высота макета.
   * Больше не зависит от высоты окна браузера.
   */
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

  align-self: end;
  justify-self: end;

  z-index: 1;

  width: 160%;

  /*
   * Не позволяем картинке заходить
   * в область логотипа.
   */
  margin-right: 0;
}

.hero__image img {
  display: block;

  width: 100%;
  height: auto;
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
    grid-template-columns: repeat(4, 1fr);

    min-height: 650px;
  }


  /* Картинка */

  .hero__image {
    grid-column: 1 / 4;
    grid-row: 1;

    align-self: end;
    justify-self: end;

    width: 120%;
  }


  /* Логотип */

  .hero__branding {
    grid-column: 1 / 5;
    grid-row: 1;

    align-self: start;

    margin-top: 100px;
  }


  .hero__branding img {
    width: min(80%, 300px);
  }


  /* Контакты */

  .hero__contacts {
    grid-column: 3 / 5;
    grid-row: 1;

    align-self: start;
    justify-self: end;

    margin-top: 20px;
    margin-right: 20px;
  }


  /* Социальные сети */

  .hero__socials {
    gap: 8px;

    margin-bottom: 12px;
  }


  .hero__social {
    width: 28px;
    height: 28px;
  }


  /* Телефон */

  .hero__phone {
    font-size: 16px;
  }


  /* Адрес */

  .hero__address {
    font-size: 13px;
  }


  .hero__second-phone {
    margin-left: 16px;
  }

}
</style>