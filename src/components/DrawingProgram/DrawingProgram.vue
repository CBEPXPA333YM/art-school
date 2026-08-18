<script setup lang="ts">

const program = [
  {
    number: 1,
    title: 'Основы композиции',
    text: 'Изучение основ композиции на листе: осевая, симметрия, асимметрия, динамика, статика, равновесие, центр, смещенный центр, контраст, нюанс.'
  },

  {
    number: 2,
    title: 'Изучение цвета',
    text: 'Цветовой круг: основные, составные цвета. Цвет в композиции. Сочетание цветов: контраст, нюанс. Теплая, холодная, нейтральные гаммы.'
  },

  {
    number: 3,
    title: 'Основы истории искусств',
    text: 'При изучении материалов, будут создаваться композиции и в качестве примеров, будут показаны работы великих мастеров изобразительного искусства.'
  },

  {
    number: 4,
    title: 'Рисование природы',
    text: 'Пейзажи времен года. Деревья, цветы, плоды. Природа разных стран и континентов.'
  },

  {
    number: 5,
    title: 'Натюрморт',
    text: 'Примеры натюрмортов: бытовые предметы, кухонная утварь, цветы, фрукты, овощи.'
  },

  {
    number: 6,
    title: 'Архитектура',
    text: 'Рисование архитектуры разных стран и исторических времен: дворцы, замки, деревни, города.'
  },

  {
    number: 7,
    title: 'Рисование человека',
    text: 'Рисование персонажей в одежде разных исторических эпох.'
  },

  {
    number: 8,
    title: 'Анималистика',
    text: 'Рисование животных, разных стран и континентов: рыбы, медведи, птицы, слоны, зайцы.'
  },

  {
    number: 9,
    title: 'Основы графического дизайна',
    text: 'Создание знаков на основе шрифтов, букв, фигур, объемов.'
  },

  {
    number: 10,
    title: 'Абстракция',
    text: 'Создание композиций на основе свободных форм: пятен, угловых, геометрических, и лекальных элементов. В основе задания может быть положен реальный сюжет: силуэт города, натюрморт, животное, что-то другое.'
  }
]

</script>


<template>

  <section id="program" class="drawing-program">

    <!-- ========================================
         TITLE
         ======================================== -->

    <h2 class="drawing-program__title">
      ПРОГРАММА. ИЗУЧЕНИЕ ОСНОВ РИСОВАНИЯ
    </h2>


    <!-- ========================================
         PROGRAM GRID
         ======================================== -->

    <div class="drawing-program__grid">

      <!-- ======================================
           PROGRAM ITEMS
           ====================================== -->

      <article
        v-for="item in program"
        :key="item.number"
        class="drawing-program__item"
      >

        <span class="drawing-program__number">
          {{ item.number }}
        </span>

        <h3 class="drawing-program__item-title">
          {{ item.title }}
        </h3>

        <p class="drawing-program__item-text">
          {{ item.text }}
        </p>

      </article>


      <!-- ======================================
           CHAMELEON
           ====================================== -->

      <div class="drawing-program__image">

        <img
          src="../../assets/images/drawing-program/chameleon.png"
          alt="Хамелеон"
        >

      </div>

    </div>

  </section>

</template>


<style lang="scss" scoped>

/* ========================================
   DRAWING PROGRAM
   ======================================== */

.drawing-program {
  width: 100%;

  padding: 80px;

  background-color: #eeedee;
}


/* ========================================
   TITLE
   ======================================== */

.drawing-program__title {
  margin: 0 0 70px;

  color: #d71920;

  font-size: 32px;
  font-weight: 700;
  line-height: 1.1;
}


/* ========================================
   GRID
   ======================================== */

.drawing-program__grid {
  display: grid;

  grid-template-columns: repeat(3, 1fr);

  column-gap: 60px;
  row-gap: 70px;

  align-items: start;
}


/* ========================================
   PROGRAM ITEM
   ======================================== */

.drawing-program__item {
  display: flex;
  flex-direction: column;

  align-items: flex-start;

  min-width: 0;

  text-align: left;
}


/* ========================================
   NUMBER
   ======================================== */

.drawing-program__number {
  display: block;

  margin-bottom: 18px;

  color: #999999;

  font-size: 180px;
  font-weight: 700;
  line-height: 0.8;

  opacity: 0.6;
}


/* ========================================
   ITEM TITLE
   ======================================== */

.drawing-program__item-title {
  margin: 0;

  color: #000000;

  font-size: 22px;
  font-weight: 700;
  line-height: 1.2;
}


/* ========================================
   ITEM TEXT
   ======================================== */

.drawing-program__item-text {
  margin: 14px 0 0;

  max-width: 400px;

  color: #000000;

  font-size: 17px;
  font-weight: 400;
  line-height: 1.5;
}


/* ========================================
   CHAMELEON
   ======================================== */

.drawing-program__image {
  grid-column: 2 / 4;

  display: flex;

  align-items: center;
  justify-content: center;

  width: 100%;
  height: 100%;

  min-height: 350px;
}


.drawing-program__image img {
  display: block;

  width: 100%;
  height: 100%;

  object-fit: contain;
  object-position: center;
}


/* ========================================
   TABLET
   ======================================== */

@media (max-width: 1000px) {

  .drawing-program {
    padding: 60px 50px;
  }


  .drawing-program__title {
    margin-bottom: 50px;

    font-size: 28px;
  }


  .drawing-program__grid {
    column-gap: 30px;
    row-gap: 50px;
  }


  .drawing-program__number {
    font-size: 140px;
  }


  .drawing-program__item-title {
    font-size: 19px;
  }


  .drawing-program__item-text {
    font-size: 15px;
  }


  .drawing-program__image {
    min-height: 280px;
  }

}


/* ========================================
   MOBILE
   ======================================== */

@media (max-width: 600px) {

  .drawing-program {
    padding: 40px 25px;
  }


  .drawing-program__title {
    margin-bottom: 40px;

    font-size: 26px;
  }


  .drawing-program__grid {
    grid-template-columns: 1fr;

    gap: 45px;
  }


  .drawing-program__number {
    font-size: 120px;

    margin-bottom: 15px;
  }


  .drawing-program__item-title {
    font-size: 20px;
  }


  .drawing-program__item-text {
    font-size: 16px;
  }


  .drawing-program__image {
    grid-column: 1;

    min-height: 300px;
  }

}

</style>