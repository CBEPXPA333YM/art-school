<template>
    <section id="works" class="gallery">
  
      <!-- ========================================
           TITLE
           ======================================== -->
  
      <h2 class="gallery__title">
        ПРИМЕРЫ РАБОТ
      </h2>
  
  
      <!-- ========================================
           WORKS
           ======================================== -->
  
      <div class="gallery__list">
  
  
        <!-- 1. Акварель -->
  
        <article class="gallery__item">
  
          <div class="gallery__image">
            <img
              src="../../assets/images/gallery/1.png"
              alt="Работа выполнена акварелью"
            >
          </div>
  
          <p class="gallery__caption">
            Акварель
          </p>
  
        </article>
  
  
        <!-- 2. Гуашь -->
  
        <article class="gallery__item">
  
          <div class="gallery__image">
            <img
              src="../../assets/images/gallery/2.png"
              alt="Работа выполнена гуашью"
            >
          </div>
  
          <p class="gallery__caption">
            Гуашь
          </p>
  
        </article>
  
  
        <!-- 3. Карандаши -->
  
        <article class="gallery__item">
  
          <div class="gallery__image">
            <img
              src="../../assets/images/gallery/3.png"
              alt="Работа выполнена карандашами"
            >
          </div>
  
          <p class="gallery__caption">
            Карандаши
          </p>
  
        </article>
  
  
        <!-- 4. Фломастеры -->
  
        <article class="gallery__item">
  
          <div class="gallery__image">
            <img
              src="../../assets/images/gallery/4.png"
              alt="Работа выполнена фломастерами"
            >
          </div>
  
          <p class="gallery__caption">
            Фломастеры
          </p>
  
        </article>
  
      </div>
  
    </section>
  </template>
  
  
  <style lang="scss" scoped>
  
  /* ========================================
     GALLERY
     ======================================== */
  
  .gallery {
    width: 100%;
  
    padding: 80px;
  
    background-color: #ffffff;
  }
  
  
  /* ========================================
     TITLE
     ======================================== */
  
  .gallery__title {
    margin: 0 0 60px;
  
    color: #d71920;
  
    font-size: 32px;
    font-weight: 700;
    line-height: 1.1;
  }
  
  
  /* ========================================
     LIST
     ======================================== */
  
  .gallery__list {
    display: grid;
  
    grid-template-columns: repeat(4, 1fr);
  
    gap: 30px;
  }
  
  
  /* ========================================
     ITEM
     ======================================== */
  
  .gallery__item {
    min-width: 0;
  }
  
  
  /* ========================================
     IMAGE
     ======================================== */
  
  .gallery__image {
    width: 100%;
  
    overflow: hidden;
  }
  
  
  .gallery__image img {
    display: block;
  
    width: 100%;
    height: auto;
  
    object-fit: contain;
  }
  
  
  /* ========================================
     CAPTION
     ======================================== */
  
  .gallery__caption {
    margin: 12px 0 0;
  
    color: #2874b8;
  
    font-size: 14px;
    font-weight: 400;
    line-height: 1.2;
  }
  
  
  /* ========================================
     TABLET
     ======================================== */
  
  @media (max-width: 1000px) {
  
    .gallery {
      padding: 60px 50px;
    }
  
  
    .gallery__title {
      margin-bottom: 50px;
  
      font-size: 28px;
    }
  
  
    .gallery__list {
      gap: 20px;
    }
  
  
    .gallery__caption {
      font-size: 13px;
    }
  
  }
  
  
  /* ========================================
     MOBILE
     ======================================== */
  
  @media (max-width: 600px) {
  
    .gallery {
      padding: 40px 25px;
    }
  
  
    .gallery__title {
      margin-bottom: 40px;
  
      font-size: 26px;
    }
  
  
    .gallery__list {
      grid-template-columns: repeat(2, 1fr);
  
      gap: 30px 20px;
    }
  
  
    .gallery__caption {
      margin-top: 8px;
  
      font-size: 13px;
    }
  
  }
  </style>