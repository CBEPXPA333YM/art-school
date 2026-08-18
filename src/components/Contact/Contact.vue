<template>

    <section
      id="contacts"
      class="contact"
    >
  
      <!-- ========================================
           MAP BACKGROUND
           ======================================== -->
  
      <img
        class="contact__map"
        src="../../assets/images/contact/Map.png"
        alt=""
      >
  
  
      <!-- ========================================
           CONTACTS
           ======================================== -->
  
      <div class="contact__content">
  
        <h2 class="contact__title">
          КОНТАКТЫ
        </h2>
  
  
        <!-- ========================================
             SOCIALS
             ======================================== -->
  
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
  
  
        <!-- ========================================
             PHONE
             ======================================== -->
  
        <a
          href="tel:+79104697054"
          class="contact__phone"
        >
          Тел.: +7 910 460 7054
        </a>
  
  
        <!-- ========================================
             ADDRESS
             ======================================== -->
  
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
  
    </section>
  
  </template>
  
  
  <style lang="scss" scoped>
  
  
  /* ========================================
     CONTACT
     ======================================== */
  
  .contact {
    position: relative;
  
    width: 100%;
  
    /*
     * Блок автоматически получает высоту
     * исходя из высоты карты.
     */
  
    overflow: hidden;
  
    background-color: #ffffff;
  }
  
  
  /* ========================================
     MAP
     ======================================== */
  
  .contact__map {
    display: block;
  
    width: 100%;
    height: auto;
  
    /*
     * Картинка сохраняет свои пропорции.
     * Ничего не обрезается.
     */
  
    object-fit: contain;
  
    pointer-events: none;
  }
  
  
  /* ========================================
     CONTENT
     ======================================== */
  
  .contact__content {
    position: absolute;
  
    top: 50%;
  
    /*
     * Расположение справа.
     */
  
    right: 8%;
  
    transform: translateY(-50%);
  
    display: flex;
    flex-direction: column;
  
    align-items: flex-start;
  
    text-align: left;
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
  
    .contact__content {
      right: 5%;
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
  
    .contact {
      /*
       * На мобильном позволяем карте
       * определять высоту блока.
       */
      overflow: visible;
    }
  
  
    .contact__map {
      width: 100%;
      height: auto;
    }
  
  
    .contact__content {
      position: absolute;
  
      top: 50%;
      right: 5%;
  
      padding: 0;
  
      transform: translateY(-50%);
    }
  
  
    .contact__title {
      font-size: 28px;
  
      margin-bottom: 25px;
    }
  
  
    .contact__socials {
      gap: 8px;
  
      margin-bottom: 18px;
    }
  
  
    .contact__social {
      width: 30px;
      height: 30px;
    }
  
  
    .contact__phone {
      font-size: 18px;
    }
  
  
    .contact__address {
      font-size: 14px;
    }
  
  
    .contact__second-phone {
      margin-left: 16px;
    }
  
  }
  
  </style>