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
            Лучшие педагоги, это не просто закончившие вузы художники,
            а художники совершенствующие свое ремесло на практике.
          </p>
  
          <p>
            По нашей программе, мы сможем научить рисовать всех,
            кто приложит терпение и желание! Приходите и вы не пожалеете!
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
  
    grid-template-columns: 1fr 2fr;
  
    align-items: center;
  
    gap: 60px;
  
    padding: 0 80px 80px;
  }
  
  
  /* ========================================
     AVATAR
     ======================================== */
  
  .teachers__avatar {
    width: 100%;
    max-width: 500px;
  
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
    display: flex;
    flex-direction: column;
  
    justify-content: center;
  
    max-width: 900px;
  
    height: 100%;
  
    color: #000000;
  
    font-size: 20px;
    font-weight: 400;
    line-height: 1.5;
  
    text-align: left;
  }
  
  
  .teachers__description p {
    margin: 0;
  }
  
  
  .teachers__description p + p {
    margin-top: 24px;
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
      gap: 40px;
  
      padding: 0 50px 60px;
    }
  
  
    .teachers__description {
      font-size: 17px;
    }
  
  
    .teachers__description p + p {
      margin-top: 18px;
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
  
  
    .teachers__profile {
      grid-template-columns: 1fr;
  
      gap: 30px;
  
      padding: 0 25px 40px;
    }
  
  
    .teachers__avatar {
      width: 100%;
      max-width: 350px;
  
      justify-self: center;
    }
  
  
    .teachers__description {
      font-size: 16px;
    }
  
  
    .teachers__description p + p {
      margin-top: 16px;
    }
  
  }
  
  </style>