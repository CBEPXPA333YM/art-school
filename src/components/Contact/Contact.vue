<template>

  <section
    id="contacts"
    class="contact"
  >

    <!-- ========================================
         СТРАНИЦА 1 — ВРЕМЯ ЗАНЯТИЯ
         ======================================== -->

    <div class="contact__time">

      <div class="contact__time-text">

        <span class="contact__time-gray">
          время
        </span>

        <span class="contact__time-gray">
          занятия
        </span>

        <span class="contact__time-number">
          90
        </span>

        <span class="contact__time-minutes">
          минут
        </span>

      </div>


      <div class="contact__clock">

        <img
          src="../../assets/images/contact/clock.png"
          alt=""
        >

      </div>

    </div>


    <!-- ========================================
         СТРАНИЦА 2 — АДРЕС И КОНТАКТЫ
         ======================================== -->

    <div class="contact__map-section">

      <!-- Карта -->

      <img
        class="contact__map"
        src="../../assets/images/contact/Map.png"
        alt=""
      >


      <!-- Контакты -->

      <div class="contact__content">

        <h2 class="contact__title">
          АДРЕС СТУДИИ И КОНТАКТЫ
        </h2>


        <!-- Социальные сети -->

        <div class="contact__socials">

          <a
            href="#"
            class="contact__social"
            aria-label="VK"
          >
            <img
              src="../../assets/images/hero/social/vk.png"
              alt="VK"
            >
          </a>

          <a
            href="#"
            class="contact__social"
            aria-label="Instagram"
          >
            <img
              src="../../assets/images/hero/social/instagram.png"
              alt="Instagram"
            >
          </a>

          <a
            href="#"
            class="contact__social"
            aria-label="Facebook"
          >
            <img
              src="../../assets/images/hero/social/facebook.png"
              alt="Facebook"
            >
          </a>

          <a
            href="#"
            class="contact__social"
            aria-label="WhatsApp"
          >
            <img
              src="../../assets/images/hero/social/whatsapp.png"
              alt="WhatsApp"
            >
          </a>

          <a
            href="#"
            class="contact__social"
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
          class="contact__phone"
        >
          Тел.: +7 910 460 7054
        </a>


        <!-- Адрес -->

        <address class="contact__address">

          Адрес: Библиотека №3<br>

          Московская область<br>

          г. Мытищи, ул. Силикатная, д. 37<br>

          тел.: +7 910 469 7054<br>

          <span class="contact__second-phone">
            +7 (495) 583 7 34 1
          </span><br>

          mail: lsbigwings@gmail.com<br>

          <span class="contact__second-phone">
            biblioteka_3@mail.ru
          </span><br>

        </address>

      </div>

    </div>

  </section>

</template>


<style lang="scss" scoped>


/* ========================================
   CONTACT
   ======================================== */

.contact {
  width: 100%;

  background-color: #ffffff;
}


/* ========================================
   СТРАНИЦА 1
   ======================================== */

.contact__time {
  display: grid;

  grid-template-columns: 1fr 1fr;

  width: 100%;

  background-color: #ffffff;
}


/* ========================================
   ТЕКСТ ВРЕМЕНИ
   ======================================== */

.contact__time-text {
  display: flex;
  flex-direction: column;

  align-items: center;
  justify-content: center;

  text-align: center;
}


/* Серые слова */

.contact__time-gray {
  display: block;

  color: #999999;

  font-size: 80px;
  font-weight: 400;

  line-height: 0.9;
}


/* 90 */

.contact__time-number {
  display: block;

  margin-top: 5px;

  color: #d71920;

  font-size: 300px;
  font-weight: 700;

  line-height: 0.75;

  text-decoration: underline;
}


/* минут */

.contact__time-minutes {
  display: block;

  margin-top: 35px;

  color: #d71920;

  font-size: 80px;
  font-weight: 400;

  line-height: 0.9;
}


/* ========================================
   CLOCK
   ======================================== */

.contact__clock {
  display: flex;

  align-items: center;
  justify-content: center;

  width: 100%;
}

.contact__clock img {
  display: block;

  width: 100%;
  height: auto;

  max-width: 700px;
}


/* ========================================
   СТРАНИЦА 2 — MAP
   ======================================== */

.contact__map-section {
  position: relative;

  width: 100%;

  overflow: visible;

  background-color: #ffffff;
}


/* ========================================
   MAP
   ======================================== */

.contact__map {
  display: block;

  width: 100%;
  height: auto;

  max-width: none;

  object-fit: contain;

  pointer-events: none;
}


/* ========================================
   CONTENT
   ======================================== */

.contact__content {
  position: absolute;

  top: 50%;
  left: 8%;

  transform: translateY(-50%);

  display: flex;
  flex-direction: column;

  align-items: flex-start;

  text-align: left;

  z-index: 2;
}


/* ========================================
   TITLE
   ======================================== */

.contact__title {
  margin: 0 0 30px;

  color: #d71920;

  font-size: 36px;
  font-weight: 700;

  line-height: 1.1;

  white-space: nowrap;
}


/* ========================================
   SOCIALS
   ======================================== */

.contact__socials {
  display: flex;

  align-items: center;

  gap: 14px;

  margin-bottom: 24px;
}


.contact__social {
  display: flex;

  align-items: center;
  justify-content: center;

  width: 40px;
  height: 40px;
}


.contact__social img {
  display: block;

  width: 100%;
  height: 100%;

  object-fit: contain;
}


/* ========================================
   PHONE
   ======================================== */

.contact__phone {
  display: block;

  color: #000000;

  font-size: 24px;
  font-weight: 600;

  line-height: 1.3;

  text-decoration: none;

  transition: opacity 0.2s ease;
}


.contact__phone:hover {
  opacity: 0.6;
}


/* ========================================
   ADDRESS
   ======================================== */

.contact__address {
  margin: 14px 0 0;

  color: #000000;

  font-size: 18px;
  font-weight: 400;

  line-height: 1.4;

  font-style: normal;

  text-align: left;
}


/* ========================================
   SECOND PHONE / EMAIL
   ======================================== */

.contact__second-phone {
  display: inline-block;

  margin-left: 44px;
}


/* ========================================
   TABLET
   ======================================== */

@media (max-width: 1000px) {

  /* Время */

  .contact__time-gray,
  .contact__time-minutes {
    font-size: 60px;
  }


  .contact__time-number {
    font-size: 220px;
  }


  .contact__clock img {
    max-width: 500px;
  }


  /* Контакты */

  .contact__content {
    left: 5%;
  }


  .contact__title {
    font-size: 30px;
  }


  .contact__social {
    width: 34px;
    height: 34px;
  }


  .contact__phone {
    font-size: 20px;
  }


  .contact__address {
    font-size: 16px;
  }

}


/* ========================================
   MOBILE
   ======================================== */

   @media (max-width: 600px) {

/* ======================================
   СТРАНИЦА 1 — ВРЕМЯ
   ====================================== */

.contact__time {
  grid-template-columns: 1fr;

  padding: 40px 0 50px;
}


.contact__time-text {
  order: 1;
}


.contact__clock {
  order: 2;

  margin-top: 30px;
}


.contact__time-gray,
.contact__time-minutes {
  font-size: 50px;
}


.contact__time-number {
  font-size: 180px;
}


.contact__clock img {
  width: 80%;
  max-width: 400px;
}


/* ======================================
   СТРАНИЦА 2 — КАРТА
   ====================================== */

.contact__map-section {
  position: relative;

  width: 100%;
  height: 650px;

  overflow: hidden;

  background-color: #ffffff;
}


/* ======================================
   КАРТА
   ====================================== */

.contact__map {
  position: absolute;

  top: 0;
  left: 50%;

  width: auto;
  height: 100%;

  max-width: none;

  transform: translateX(-50%);

  object-fit: cover;

  z-index: 1;
}


/* ======================================
   КОНТАКТЫ
   ====================================== */

.contact__content {
  position: absolute;

  top: 50%;
  left: 5%;
  right: 5%;

  width: auto;
  max-width: none;

  transform: translateY(-50%);

  display: flex;
  flex-direction: column;

  align-items: center;

  text-align: center;

  z-index: 2;
}


/* ======================================
   ЗАГОЛОВОК
   ====================================== */

.contact__title {
  margin: 0 0 20px;

  font-size: 24px;

  line-height: 1.1;

  white-space: normal;
}


/* ======================================
   СОЦИАЛЬНЫЕ СЕТИ
   ====================================== */

.contact__socials {
  gap: 8px;

  margin-bottom: 18px;
}


.contact__social {
  width: 30px;
  height: 30px;
}


/* ======================================
   ТЕЛЕФОН
   ====================================== */

.contact__phone {
  font-size: 18px;
}


/* ======================================
   АДРЕС
   ====================================== */

.contact__address {
  margin-top: 10px;

  font-size: 14px;
  line-height: 1.4;

  text-align: center;
}


.contact__second-phone {
  margin-left: 0;
}

}
</style>