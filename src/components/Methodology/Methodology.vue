<template>
    <section id="methodology" class="methodology">
  
      <!-- ========================================
           TITLE
           ======================================== -->
  
      <h2 class="methodology__title">
        МЕТОДИКА ШКОЛЫ
      </h2>
  
  
      <!-- ========================================
           METHODOLOGY ITEMS
           ======================================== -->
  
      <div class="methodology__list">
  
  
        <!-- ======================================
             1. Индивидуальный подход
             ====================================== -->
  
        <article class="methodology__item">
  
          <span class="methodology__number">
            1
          </span>
  
          <h3 class="methodology__item-title">
            Индивидуальный подход
          </h3>
  
          <p class="methodology__item-text">
            У всех начинающих учиться изобразительному искусству
            разные способности. Кто-то просто теряется и не знает
            что делать. Поэтому для каждого создается персональная
            программа.
          </p>
  
        </article>
  
  
        <!-- ======================================
             2. От простого к сложному
             ====================================== -->
  
        <article class="methodology__item">
  
          <span class="methodology__number">
            2
          </span>
  
          <h3 class="methodology__item-title">
            От простого к сложному
          </h3>
  
          <p class="methodology__item-text">
            В основе преподавания рисования – метод от простого
            к сложному, на основе простых форм, который будет
            понятен каждому и даст возможность пошагово
            постигать знания.
          </p>
  
        </article>
  
  
        <!-- ======================================
             3. Вовлечение в творчество
             ====================================== -->
  
        <article class="methodology__item">
  
          <span class="methodology__number">
            3
          </span>
  
          <h3 class="methodology__item-title">
            Вовлечение в творчество
          </h3>
  
          <p class="methodology__item-text">
            Главной целью рисовальной школы знаний является
            раскрытие творческого потенциала ребенка,
            так необходимого в жизни.
          </p>
  
        </article>
  
      </div>
  
    </section>
  </template>
  
  
  <style lang="scss" scoped>
  
  /* ========================================
     METHODOLOGY
     ======================================== */
  
  .methodology {
    width: 100%;
  
    padding: 80px;
  
    background-color: #eeedee;
  }
  
  
  /* ========================================
     TITLE
     ======================================== */
  
  .methodology__title {
    margin: 0 0 60px;
  
    color: #d71920;
  
    font-size: 32px;
    font-weight: 700;
    line-height: 1.1;
  }
  
  
  /* ========================================
     LIST
     ======================================== */
  
  .methodology__list {
    display: grid;
  
    grid-template-columns: repeat(3, 1fr);
  
    gap: 60px;
  }
  
  
  /* ========================================
     ITEM
     ======================================== */
  
  .methodology__item {
    display: flex;
    flex-direction: column;
  
    align-items: flex-start;
  
    text-align: left;
  }
  
  
  /* ========================================
     NUMBER
     ======================================== */
  
  .methodology__number {
    display: block;
  
    margin-bottom: 15px;
  
    color: #999999;
  
    font-size: 180px;
    font-weight: 700;
    line-height: 0.8;
  
    opacity: 0.6;
  }
  
  
  /* ========================================
     ITEM TITLE
     ======================================== */
  
  .methodology__item-title {
    margin: 0;
  
    color: #000000;
  
    font-size: 22px;
    font-weight: 700;
    line-height: 1.2;
  }
  
  
  /* ========================================
     ITEM TEXT
     ======================================== */
  
  .methodology__item-text {
    margin: 14px 0 0;
  
    max-width: 400px;
  
    color: #000000;
  
    font-size: 17px;
    font-weight: 400;
    line-height: 1.5;
  }
  
  
  /* ========================================
     TABLET
     ======================================== */
  
  @media (max-width: 1000px) {
  
    .methodology {
      padding: 60px 50px;
    }
  
  
    .methodology__title {
      margin-bottom: 50px;
  
      font-size: 28px;
    }
  
  
    .methodology__list {
      gap: 30px;
    }
  
  
    .methodology__number {
      font-size: 140px;
    }
  
  
    .methodology__item-title {
      font-size: 19px;
    }
  
  
    .methodology__item-text {
      font-size: 15px;
    }
  
  }
  
  
  /* ========================================
     MOBILE
     ======================================== */
  
  @media (max-width: 600px) {
  
    .methodology {
      padding: 40px 25px;
    }
  
  
    .methodology__title {
      margin-bottom: 40px;
  
      font-size: 26px;
    }
  
  
    .methodology__list {
      grid-template-columns: 1fr;
  
      gap: 45px;
    }
  
  
    .methodology__number {
      font-size: 120px;
  
      margin-bottom: 15px;
    }
  
  
    .methodology__item-title {
      font-size: 20px;
    }
  
  
    .methodology__item-text {
      font-size: 16px;
    }
  
  }
  </style>