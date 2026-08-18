<template>
  <section id="about" class="about-studio">

    <!-- ========================================
         О СТУДИИ
         ======================================== -->

    <div class="about-studio__intro">

      <div class="about-studio__content">

        <h2 class="about-studio__title">
          О СТУДИИ
        </h2>

        <p class="about-studio__subtitle">
          ВСЕ ДЕТИ УМЕЮТ РИСОВАТЬ, НО ВЫ ЕЩЁ ОБ ЭТОМ НЕ ЗНАЕТЕ.
        </p>

        <p class="about-studio__description">
          Студия изобразительного искусства «Большие крылья» предлагает
          уникальные возможности для развития творческих способностей детей,
          формирования художественно-образного мышления, эстетического вкуса.
          Особенности обучения включают интеграцию разных видов
          визуально-пространственных искусств, таких как живопись, графика,
          дизайн.
        </p>

      </div>


      <!-- Вишня -->

      <div class="about-studio__intro-image">
        <img
          src="../../assets/images/about-studio/cherry.png"
          alt="Занятие в изостудии"
        >
      </div>

    </div>


    <!-- ========================================
         ВЫ СМОЖЕТЕ
         ======================================== -->

    <div class="about-studio__advantages">

      <h2 class="about-studio__advantages-title">
        ВЫ СМОЖЕТЕ
      </h2>


      <!-- Рыба -->

      <div class="about-studio__advantages-image">
        <img
          src="../../assets/images/about-studio/fish.png"
          alt=""
        >
      </div>


      <!-- Три преимущества -->

      <div class="about-studio__advantages-list">

        <!-- 1 -->

        <article class="about-studio__advantage">

          <span class="about-studio__number">
            1
          </span>

          <h3 class="about-studio__advantage-title">
            Создавать композиции
          </h3>

          <p class="about-studio__advantage-text">
            Узнать основы простой и сложной композиции.
            Значение пятна, линии и цвета в рисунке.
          </p>

        </article>


        <!-- 2 -->

        <article class="about-studio__advantage">

          <span class="about-studio__number">
            2
          </span>

          <h3 class="about-studio__advantage-title">
            Передавать объем
          </h3>

          <p class="about-studio__advantage-text">
            Научитесь передавать объем линией, тоном, цветом.
            Сможете передавать форму минимальными средствами.
          </p>

        </article>


        <!-- 3 -->

        <article class="about-studio__advantage">

          <span class="about-studio__number">
            3
          </span>

          <h3 class="about-studio__advantage-title">
            Быстро зарисовывать
          </h3>

          <p class="about-studio__advantage-text">
            Будете создавать быстрые наброски и рисунки.
            Это поможет вам быстро создавать эскизы будущих произведений.
          </p>

        </article>

      </div>

    </div>

  </section>
</template>


<style lang="scss" scoped>

/* ========================================
   ABOUT STUDIO
   ======================================== */

.about-studio {
  width: 100%;
}


/* ========================================
   INTRO
   ======================================== */

.about-studio__intro {
  display: grid;

  grid-template-columns: 2fr 1fr;

  width: 100%;

  background-color: #eeedee;
}


/* ========================================
   INTRO CONTENT
   ======================================== */

.about-studio__content {
  display: flex;
  flex-direction: column;

  justify-content: center;

  padding: 80px;
}


/* ========================================
   TITLE
   ======================================== */

.about-studio__title {
  margin: 0;

  color: #d71920;

  font-size: 32px;
  font-weight: 700;
  line-height: 1.1;
}


/* ========================================
   SUBTITLE
   ======================================== */

.about-studio__subtitle {
  margin: 18px 0 0;

  color: #000000;

  font-size: 27px;
  font-weight: 400;
  line-height: 1.2;

  text-align: left;
}


/* ========================================
   DESCRIPTION
   ======================================== */

.about-studio__description {
  margin: 24px 0 0;

  max-width: 900px;

  color: #000000;

  font-size: 18px;
  font-weight: 400;
  line-height: 1.5;

  text-align: left;
}


/* ========================================
   CHERRY
   ======================================== */

.about-studio__intro-image {
  width: 100%;
  height: 100%;
}

.about-studio__intro-image img {
  display: block;

  width: 100%;
  height: 100%;

  object-fit: cover;
  object-position: center;
}


/* ========================================
   ADVANTAGES
   ======================================== */

.about-studio__advantages {
  position: relative;

  width: 100%;

  padding: 80px;

  overflow: hidden;

  background-color: #ffffff;
}


/* ========================================
   ADVANTAGES TITLE
   ======================================== */

.about-studio__advantages-title {
  position: relative;

  z-index: 2;

  margin: 0 0 50px;

  color: #d71920;

  font-size: 32px;
  font-weight: 700;
  line-height: 1.1;
}


/* ========================================
   FISH
   ======================================== */

.about-studio__advantages-image {
  position: absolute;

  top: 0;
  left: 50%;

  z-index: 0;

  width: 100vh;
  height: 100vh;

  transform: translateX(-50%);

  pointer-events: none;
}

.about-studio__advantages-image img {
  display: block;

  width: 100%;
  height: 100%;

  object-fit: contain;
  object-position: top center;
}


/* ========================================
   ADVANTAGES LIST
   ======================================== */

.about-studio__advantages-list {
  position: relative;

  z-index: 1;

  display: grid;

  grid-template-columns: repeat(3, 1fr);

  gap: 60px;
}


/* ========================================
   ADVANTAGE
   ======================================== */

.about-studio__advantage {
  display: flex;
  flex-direction: column;

  align-items: flex-start;

  text-align: left;
}


/* ========================================
   NUMBER
   ======================================== */

.about-studio__number {
  display: block;

  margin-bottom: 15px;

  color: #999999;

  font-size: 180px;
  font-weight: 700;
  line-height: 0.8;

  opacity: 0.6;
}


/* ========================================
   ADVANTAGE TITLE
   ======================================== */

.about-studio__advantage-title {
  margin: 0;

  color: #000000;

  font-size: 22px;
  font-weight: 700;
  line-height: 1.2;
}


/* ========================================
   ADVANTAGE TEXT
   ======================================== */

.about-studio__advantage-text {
  margin: 14px 0 0;

  max-width: 350px;

  color: #000000;

  font-size: 17px;
  font-weight: 400;
  line-height: 1.5;
}


/* ========================================
   TABLET
   ======================================== */

@media (max-width: 1000px) {

  .about-studio__content {
    padding: 50px;
  }


  .about-studio__title,
  .about-studio__advantages-title {
    font-size: 28px;
  }


  .about-studio__subtitle {
    font-size: 23px;
  }


  .about-studio__description {
    font-size: 16px;
  }


  .about-studio__advantages {
    padding: 50px;
  }


  .about-studio__advantages-list {
    gap: 30px;
  }


  .about-studio__number {
    font-size: 140px;
  }


  .about-studio__advantage-title {
    font-size: 19px;
  }


  .about-studio__advantage-text {
    font-size: 15px;
  }


  .about-studio__advantages-image {
    left: 45%;

    width: 50vh;
    height: 50vh;

    max-height: 50vh;
  }

}


/* ========================================
   MOBILE
   ======================================== */

@media (max-width: 600px) {

  .about-studio__intro {
    grid-template-columns: 1fr;
  }


  .about-studio__content {
    padding: 40px 25px;
  }


  .about-studio__title,
  .about-studio__advantages-title {
    font-size: 26px;
  }


  .about-studio__subtitle {
    font-size: 21px;
  }


  .about-studio__description {
    font-size: 16px;
  }


  .about-studio__intro-image {
    height: 300px;
  }


  /* ======================================
     ADVANTAGES
     ====================================== */

  .about-studio__advantages {
    padding: 40px 25px;
  }


  .about-studio__advantages-title {
    margin-bottom: 30px;
  }


  .about-studio__advantages-list {
    grid-template-columns: 1fr;

    gap: 40px;
  }


  .about-studio__number {
    font-size: 120px;

    margin-bottom: 15px;
  }


  .about-studio__advantage-title {
    font-size: 20px;
  }


  .about-studio__advantage-text {
    font-size: 16px;
  }


  /* ======================================
     FISH
     ====================================== */

  .about-studio__advantages-image {
    position: absolute;

    top: 0;
    left: 50%;

    width: 300px;
    height: 300px;

    max-height: 300px;

    transform: translateX(-50%);
  }

}

</style>