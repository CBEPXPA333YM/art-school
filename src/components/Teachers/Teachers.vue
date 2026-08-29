<template>
  <section id="teachers" class="teachers">

    <!-- ========================================
         TITLE
         ======================================== -->

    <h2 class="teachers__title">
      ПЕДАГОГИ ПРОФЕССИОНАЛЫ
    </h2>


    <!-- ========================================
         TEACHER
         ======================================== -->

    <div class="teachers__profile">

      <!-- Аватар -->

      <div class="teachers__avatar">
        <img
          src="../../assets/images/teachers/teacher.png"
          alt="Сергей Александрович Лебедев"
        >
      </div>


      <!-- Текст -->

      <div class="teachers__description">

        <p>
        Чтобы передавать знания, нужно хорошо знать предмет.
        Лучшие педагоги — это не просто закончившие вузы художники,
        а художники, совершенствующие свое ремесло на практике.
        По нашей программе мы сможем научить рисовать всех,
        кто приложит терпение и желание! Приходите, и вы не пожалеете!
        </p>

        <p>
        Занятия ведет художник, дизайнер, член Московского союза
        художников России, секции «Промграфика»
        Сергей Александрович Лебедев.
        </p>

      </div>

    </div>


    <!-- ========================================
         LESSON IMAGE
         ======================================== -->

    <div class="teachers__lesson">
      <img
        src="../../assets/images/teachers/lesson.png"
        alt="Занятие в изостудии"
      >
    </div>

  </section>
</template>


<style lang="scss" scoped>

/* ========================================
   TEACHERS
   ======================================== */

.teachers {
  width: 100%;

  background-color: #eeedee;
}


/* ========================================
   TITLE
   ======================================== */

.teachers__title {
  margin: 0;

  padding: 80px 80px 50px;

  color: #d71920;

  font-size: 32px;
  font-weight: 700;
  line-height: 1.1;
}


/* ========================================
   TEACHER PROFILE
   ======================================== */

.teachers__profile {
  display: grid;

  /*
   * Аватар занимает небольшую часть
   * пространства, текст — основную.
   */

  grid-template-columns: 1fr 5fr;

  align-items: center;

  gap: 60px;

  padding: 0 80px 80px;
}


/* ========================================
   AVATAR
   ======================================== */

.teachers__avatar {
  width: 100%;
  max-width: 180px;

  justify-self: end;

  aspect-ratio: 1 / 1;

  overflow: hidden;
}


.teachers__avatar img {
  display: block;

  width: 100%;
  height: 100%;

  object-fit: cover;
  object-position: center;
}


/* ========================================
   DESCRIPTION
   ======================================== */

.teachers__description {
  max-width: 1000px;

  color: #000000;

  font-size: 20px;
  font-weight: 400;
  line-height: 1.5;

  text-align: left;
}


.teachers__description p {
  margin: 0;
}


/* ========================================
   LESSON IMAGE
   ======================================== */

.teachers__lesson {
  width: 100%;

  overflow: hidden;
}


.teachers__lesson img {
  display: block;

  width: 100%;
  height: auto;

  object-fit: cover;
}


/* ========================================
   TABLET
   ======================================== */

@media (max-width: 1000px) {

  .teachers__title {
    padding: 60px 50px 40px;

    font-size: 28px;
  }


  .teachers__profile {
    grid-template-columns: 140px 1fr;

    gap: 40px;

    padding: 0 50px 60px;
  }


  .teachers__avatar {
    max-width: 140px;
  }


  .teachers__description {
    font-size: 17px;
  }

}

/* ========================================
   MOBILE
   ======================================== */

   @media (max-width: 600px) {

.teachers__title {
  padding: 40px 25px 30px;

  font-size: 26px;
}


/* ========================================
   PROFILE
   ======================================== */

.teachers__profile {
  display: block;

  padding: 0 25px 40px;
}


/* ========================================
   AVATAR
   ======================================== */

.teachers__avatar {
  float: left;

  width: 110px;
  max-width: 110px;

  height: 110px;

  margin: 0 20px 10px 0;

  aspect-ratio: 1 / 1;

  overflow: hidden;
}


.teachers__avatar img {
  display: block;

  width: 100%;
  height: 100%;

  object-fit: cover;
  object-position: center;
}


/* ========================================
   DESCRIPTION
   ======================================== */

.teachers__description {
  max-width: none;

  font-size: 16px;
  line-height: 1.5;

  text-align: left;
}


.teachers__description p {
  margin: 0;
}


/* ========================================
   LESSON
   ======================================== */

.teachers__lesson {
  clear: both;

  width: 100%;
}

}

</style>