<script setup lang="ts">

const leftItems = [
  {
    number: 1,
    title: 'Простой карандаш',
    text: `
      Рисование линий, пятен, изучение основ штриха
      и композиции.
    `
  },

  {
    number: 2,
    title: 'Цветные карандаши',
    text: `
      Работа с цветом и цветовой композицией.
      Изучение техники работы с цветными карандашами:
      линия, пятно, цвет.
    `
  },

  {
    number: 3,
    title: 'Акварельные краски',
    text: `
      Изучение техники акварели: по сырому, по сухому,
      мазок, пятно. Декоративность в акварели.
      Понимание фактуры, как эстетического свойства акварели.
    `
  },

  {
    number: 4,
    title: 'Гуашь',
    text: `
      Изучение техники гуаши и ее возможности как
      перекрывающей краски. Умение смешивать краски
      в необходимой пропорции и разведении водой.
    `
  }
]


const rightItems = [
  {
    number: 5,
    title: 'Импровизации на тему “Современное искусство”',
    text: `
      Современные импровизации с использованием разных техник:
      карандаши, фломастеры, краска и другое, для создания
      разных композиций.
    `
  },

  {
    number: 6,
    title: 'Аппликация',
    text: `
      Создание композиций из цветной бумаги,
      фрагментов газет и журналов.
    `
  },

  {
    number: 7,
    title: 'Фломастер',
    text: `
      Изучение техники фломастеров: круглых, плоских,
      разной толщины и создание композиций данными материалами.
    `
  },

  {
    number: 8,
    title: 'Объем. Бумага',
    text: `
      Создание фигур из бумаги: животные, цветы,
      геометрические объемы.
    `
  }
]

</script>


<template>

  <section
    id="materials"
    class="materials-techniques"
  >

    <!-- ========================================
         TITLE
         ======================================== -->

    <h2 class="materials-techniques__title">
      ИЗУЧЕНИЕ МАТЕРИАЛОВ И ТЕХНИК.
      ЗАДАЧИ И ОСНОВЫ
    </h2>


    <!-- ========================================
         TWO COLUMNS
         ======================================== -->

    <div class="materials-techniques__columns">


      <!-- ======================================
           LEFT COLUMN
           ====================================== -->

      <div class="materials-techniques__column">

        <article
          v-for="item in leftItems"
          :key="item.number"
          class="materials-techniques__item"
        >

          <h3 class="materials-techniques__item-title">
            {{ item.number }}. {{ item.title }}
          </h3>

          <p class="materials-techniques__item-text">
            {{ item.text }}
          </p>

        </article>

      </div>


      <!-- ======================================
           RIGHT COLUMN
           ====================================== -->

      <div class="materials-techniques__column">

        <article
          v-for="item in rightItems"
          :key="item.number"
          class="materials-techniques__item"
        >

          <h3 class="materials-techniques__item-title">
            {{ item.number }}. {{ item.title }}
          </h3>

          <p class="materials-techniques__item-text">
            {{ item.text }}
          </p>

        </article>

      </div>

    </div>

  </section>

</template>


<style lang="scss" scoped>

/* ========================================
   SECTION
   ======================================== */

.materials-techniques {
  width: 100%;

  padding: 80px;

  background-color: #ffffff;
}


/* ========================================
   TITLE
   ======================================== */

.materials-techniques__title {
  margin: 0 0 70px;

  color: #d71920;

  font-size: 32px;
  font-weight: 700;
  line-height: 1.1;

  text-align: left;
}


/* ========================================
   COLUMNS
   ======================================== */

.materials-techniques__columns {
  display: grid;

  grid-template-columns: repeat(2, 1fr);

  gap: 100px;
}


/* ========================================
   COLUMN
   ======================================== */

.materials-techniques__column {
  display: flex;
  flex-direction: column;

  gap: 45px;
}


/* ========================================
   ITEM
   ======================================== */

.materials-techniques__item {
  max-width: 650px;
}


/* ========================================
   ITEM TITLE
   ======================================== */

.materials-techniques__item-title {
  margin: 0;

  color: #000000;

  font-size: 22px;
  font-weight: 700;
  line-height: 1.25;
}


/* ========================================
   ITEM TEXT
   ======================================== */

.materials-techniques__item-text {
  margin: 12px 0 0;

  color: #000000;

  font-size: 17px;
  font-weight: 400;
  line-height: 1.5;

  white-space: pre-line;
}


/* ========================================
   TABLET
   ======================================== */

@media (max-width: 1000px) {

  .materials-techniques {
    padding: 60px 50px;
  }


  .materials-techniques__title {
    margin-bottom: 50px;

    font-size: 28px;
  }


  .materials-techniques__columns {
    gap: 50px;
  }


  .materials-techniques__column {
    gap: 35px;
  }


  .materials-techniques__item-title {
    font-size: 19px;
  }


  .materials-techniques__item-text {
    font-size: 15px;
  }

}


/* ========================================
   MOBILE
   ======================================== */

@media (max-width: 600px) {

  .materials-techniques {
    padding: 40px 25px;
  }


  .materials-techniques__title {
    margin-bottom: 40px;

    font-size: 26px;
  }


  .materials-techniques__columns {
    grid-template-columns: 1fr;

    gap: 45px;
  }


  .materials-techniques__column {
    gap: 35px;
  }


  .materials-techniques__item-title {
    font-size: 20px;
  }


  .materials-techniques__item-text {
    font-size: 16px;
  }

}

</style>