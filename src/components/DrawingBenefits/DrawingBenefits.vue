<template>
    <section id="benefits" class="drawing-benefits">
  
      <!-- ========================================
           TITLE
           ======================================== -->
  
      <h2 class="drawing-benefits__title">
        РИСОВАНИЕ – ДЛЯ РАЗВИТИЯ
      </h2>
  
  
      <!-- ========================================
           BENEFITS GRID
           ======================================== -->
  
      <div class="drawing-benefits__grid">
  
        <!-- ======================================
             1. Понимание современного искусства
             ====================================== -->
  
        <article class="drawing-benefits__item">
  
          <div class="drawing-benefits__image">
            <img
              src="../../assets/images/drawing-benefits/1.png"
              alt="Понимание современного искусства"
            >
          </div>
  
          <h3 class="drawing-benefits__text">
            Понимание современного искусства
          </h3>
  
        </article>
  
  
        <!-- ======================================
             2. Рисование – проведение свободного времени
             ====================================== -->
  
        <article class="drawing-benefits__item">
  
          <div class="drawing-benefits__image">
            <img
              src="../../assets/images/drawing-benefits/2.png"
              alt="Рисование – проведение свободного времени"
            >
          </div>
  
          <h3 class="drawing-benefits__text">
            Рисование – проведение свободного времени
          </h3>
  
        </article>
  
  
        <!-- ======================================
             3. Развитие моторики рук
             ====================================== -->
  
        <article class="drawing-benefits__item">
  
          <div class="drawing-benefits__image">
            <img
              src="../../assets/images/drawing-benefits/3.png"
              alt="Развитие моторики рук"
            >
          </div>
  
          <h3 class="drawing-benefits__text">
            Развитие моторики рук
          </h3>
  
        </article>
  
  
        <!-- ======================================
             4. Развитие образного мышления
             ====================================== -->
  
        <article class="drawing-benefits__item">
  
          <div class="drawing-benefits__image">
            <img
              src="../../assets/images/drawing-benefits/4.png"
              alt="Развитие образного мышления"
            >
          </div>
  
          <h3 class="drawing-benefits__text">
            Развитие образного мышления
          </h3>
  
        </article>
  
      </div>
  
    </section>
  </template>
  
  
  <style lang="scss" scoped>
  
  /* ========================================
     DRAWING BENEFITS
     ======================================== */
  
  .drawing-benefits {
    width: 100%;
  
    padding: 80px;
  
    background-color: #ffffff;
  }
  
  
  /* ========================================
     TITLE
     ======================================== */
  
  .drawing-benefits__title {
    margin: 0 0 70px;
  
    color: #d71920;
  
    font-size: 32px;
    font-weight: 700;
    line-height: 1.1;
  }
  
  
  /* ========================================
     GRID
     ======================================== */
  
  .drawing-benefits__grid {
    display: grid;
  
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(2, auto);
  
    column-gap: 100px;
    row-gap: 80px;
  }
  
  
  /* ========================================
     ITEM
     ======================================== */
  
  .drawing-benefits__item {
    display: flex;
    flex-direction: column;
  
    align-items: flex-start;
  
    text-align: left;
  }
  
  
  /* ========================================
     IMAGE
     ======================================== */
  
  .drawing-benefits__image {
    width: 100%;
  
    display: flex;
  
    align-items: center;
    justify-content: center;
  }
  
  
  .drawing-benefits__image img {
    display: block;
  
    width: auto;
    max-width: 100%;
  
    height: auto;
  
    object-fit: contain;
  }
  
  
  /* ========================================
     TEXT
     ======================================== */
  
  .drawing-benefits__text {
    margin: 24px 0 0;
  
    max-width: 500px;
  
    color: #000000;
  
    font-size: 22px;
    font-weight: 700;
    line-height: 1.25;
  
    text-align: left;
  }
  
  
  /* ========================================
     TABLET
     ======================================== */
  
  @media (max-width: 1000px) {
  
    .drawing-benefits {
      padding: 60px 50px;
    }
  
  
    .drawing-benefits__title {
      margin-bottom: 50px;
  
      font-size: 28px;
    }
  
  
    .drawing-benefits__grid {
      column-gap: 50px;
      row-gap: 60px;
    }
  
  
    .drawing-benefits__text {
      margin-top: 18px;
  
      font-size: 19px;
    }
  
  }
  
  
  /* ========================================
     MOBILE
     ======================================== */
  
  @media (max-width: 600px) {
  
    .drawing-benefits {
      padding: 40px 25px;
    }
  
  
    .drawing-benefits__title {
      margin-bottom: 40px;
  
      font-size: 26px;
    }
  
  
    .drawing-benefits__grid {
      grid-template-columns: 1fr;
  
      gap: 45px;
    }
  
  
    .drawing-benefits__item {
      align-items: center;
  
      text-align: center;
    }
  
  
    .drawing-benefits__text {
      max-width: 400px;
  
      font-size: 18px;
  
      text-align: center;
    }
  
  }
  </style>