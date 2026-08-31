```vue
<template>

  <section class="lesson-time">

    <div class="lesson-time__text">

      <span class="lesson-time__gray">
        время
      </span>

      <span class="lesson-time__gray">
        занятия
      </span>

      <span class="lesson-time__number">
        90
      </span>

      <span class="lesson-time__minutes">
        минут
      </span>

    </div>


    <div class="lesson-time__clock">

      <img
        src="../../assets/images/contact/clock.png"
        alt="90 минут"
      >

    </div>

  </section>

</template>


<style lang="scss" scoped>

.lesson-time {
  display: grid;

  grid-template-columns: 1fr 1fr;

  width: 100%;

  background-color: #ffffff;
}


/* ========================================
   ТЕКСТ
   ======================================== */

.lesson-time__text {
  display: flex;

  flex-direction: column;

  align-items: center;
  justify-content: center;

  text-align: center;
}


.lesson-time__gray {
  display: block;

  color: #999999;

  font-size: 80px;
  font-weight: 400;

  line-height: 0.9;
}


.lesson-time__number {
  display: block;

  margin-top: 5px;

  color: #d71920;

  font-size: 300px;
  font-weight: 700;

  line-height: 0.75;

  text-decoration: underline;
}


.lesson-time__minutes {
  display: block;

  margin-top: 35px;

  color: #d71920;

  font-size: 80px;
  font-weight: 400;

  line-height: 0.9;
}


/* ========================================
   ЧАСЫ
   ======================================== */

.lesson-time__clock {
  display: flex;

  align-items: center;
  justify-content: center;

  width: 100%;
}


.lesson-time__clock img {
  display: block;

  width: 100%;
  height: auto;

  max-width: 700px;
}


/* ========================================
   TABLET
   ======================================== */

@media (max-width: 1000px) {

  .lesson-time__gray,
  .lesson-time__minutes {
    font-size: 60px;
  }


  .lesson-time__number {
    font-size: 220px;
  }


  .lesson-time__clock img {
    max-width: 500px;
  }

}


/* ========================================
   MOBILE
   ======================================== */

@media (max-width: 600px) {

  .lesson-time {
    grid-template-columns: 1fr;

    padding: 40px 0 50px;
  }


  .lesson-time__text {
    order: 1;
  }


  .lesson-time__clock {
    order: 2;

    margin-top: 30px;
  }


  .lesson-time__gray,
  .lesson-time__minutes {
    font-size: 50px;
  }


  .lesson-time__number {
    font-size: 180px;
  }


  .lesson-time__clock img {
    width: 80%;

    max-width: 400px;
  }

}

</style>
```
