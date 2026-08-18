<script setup lang="ts">

const scheduleRows = [
  {
    days: ['понедельник', 'среда', 'четверг'],
    times: [
      '10.15 - 11.45',
      '13.00 - 14.30',
      '15.00 - 16.30',
      '17.00 - 18.30'
    ]
  },

  {
    days: ['пятница'],
    times: [
      '10.15 - 11.45',
      '13.00 - 14.30',
      '15.00 - 16.30'
    ]
  },

  {
    days: ['суббота'],
    times: [
      '10.15 - 11.45'
    ]
  }
]


const prices = [
  {
    title: 'Одно занятие в группе',
    price: '1100'
  },

  {
    title: 'Одно индивидуальное занятие',
    price: '1600'
  },

  {
    title: 'Абонемент на 1 месяц (8 занятий)',
    price: '7800'
  },

  {
    title: 'Абонемент на 1 месяц (4 занятия)',
    price: '4000'
  }
]

</script>


<template>

  <section
    id="schedule"
    class="schedule-price"
  >

    <!-- ========================================
         TITLE
         ======================================== -->

    <h2 class="schedule-price__title">
      РАСПИСАНИЕ ЗАНЯТИЙ. СТОИМОСТЬ
    </h2>


    <!-- ========================================
         SUBTITLE
         ======================================== -->

    <p class="schedule-price__subtitle">
      Длительность занятия - 90 минут
    </p>


    <!-- ========================================
         TABLES
         ======================================== -->

    <div class="schedule-price__tables">


      <!-- ======================================
           SCHEDULE
           ====================================== -->

      <div class="schedule-price__card schedule-price__card--schedule">

        <h3 class="schedule-price__card-title">
          Расписание занятий с сентября по июль.
        </h3>


        <div class="schedule-price__schedule">

          <div
            v-for="(row, rowIndex) in scheduleRows"
            :key="rowIndex"
            class="schedule-price__schedule-row"
          >

            <!-- ДНИ -->

            <div class="schedule-price__days">

              <div
                v-for="day in row.days"
                :key="day"
                class="schedule-price__day"
              >
                {{ day }}
              </div>

            </div>


            <!-- ВРЕМЯ -->

            <div class="schedule-price__times">

              <div
                v-for="time in row.times"
                :key="time"
                class="schedule-price__time"
              >
                {{ time }}
              </div>

            </div>

          </div>

        </div>

      </div>


      <!-- ======================================
           PRICE
           ====================================== -->

      <div class="schedule-price__card schedule-price__card--price">

        <h3 class="schedule-price__card-title">
          Стоимость занятий (руб.)
        </h3>


        <div class="schedule-price__prices">

          <div
            v-for="item in prices"
            :key="item.title"
            class="schedule-price__price-row"
          >

            <div class="schedule-price__price-name">
              {{ item.title }}
            </div>

            <div class="schedule-price__price-value">
              {{ item.price }}
            </div>

          </div>

        </div>

      </div>

    </div>

  </section>

</template>


<style lang="scss" scoped>

/* ========================================
   SECTION
   ======================================== */

.schedule-price {
  width: 100%;

  padding: 80px;

  background-color: #ffeb66;
}


/* ========================================
   TITLE
   ======================================== */

.schedule-price__title {
  margin: 0;

  color: #d71920;

  font-size: 32px;
  font-weight: 700;
  line-height: 1.1;

  text-align: left;
}


/* ========================================
   SUBTITLE
   ======================================== */

.schedule-price__subtitle {
  margin: 10px 0 45px;

  color: #777777;

  font-size: 24px;
  font-weight: 700;
  line-height: 1.3;

  text-align: left;
}


/* ========================================
   TABLES
   ======================================== */

.schedule-price__tables {
  display: grid;

  grid-template-columns: 1fr 2fr;

  gap: 40px;

  align-items: stretch;
}


/* ========================================
   CARD
   ======================================== */

.schedule-price__card {
  display: flex;
  flex-direction: column;

  padding: 35px;

  background-color: transparent;

  border: 5px solid #d71920;
  border-radius: 30px;

  color: #000000;
}


/* ========================================
   CARD TITLE
   ======================================== */

.schedule-price__card-title {
  flex-shrink: 0;

  margin: 0 0 30px;

  color: #000000;

  font-size: 24px;
  font-weight: 700;
  line-height: 1.2;
}


/* ========================================
   SCHEDULE
   ======================================== */

.schedule-price__schedule {
  display: flex;
  flex-direction: column;

  flex: 1;
}


/* ========================================
   SCHEDULE ROW
   ======================================== */

.schedule-price__schedule-row {
  display: grid;

  grid-template-columns: 1fr 1fr;

  flex: 1;

  /*
   * Горизонтальная линия только
   * между большими группами.
   */
}

.schedule-price__schedule-row + .schedule-price__schedule-row {
  border-top: 2px solid #000000;
}


/* ========================================
   DAYS
   ======================================== */

.schedule-price__days {
  display: flex;
  flex-direction: column;

  justify-content: center;

  border-right: 2px solid #000000;
}


/* ========================================
   DAY
   ======================================== */

.schedule-price__day {
  padding: 8px 10px;

  font-size: 17px;
  font-weight: 400;

  line-height: 1.4;

  text-transform: lowercase;
}


/* ========================================
   TIMES
   ======================================== */

.schedule-price__times {
  display: flex;
  flex-direction: column;

  justify-content: center;
}


/* ========================================
   TIME
   ======================================== */

.schedule-price__time {
  flex: 1;

  display: flex;
  align-items: center;

  padding: 8px 10px;

  font-size: 17px;
  font-weight: 400;

  line-height: 1.4;
}/* ========================================
   SCHEDULE
   ======================================== */

.schedule-price__schedule {
  display: flex;
  flex-direction: column;

  flex: 1;
}


/* ========================================
   SCHEDULE ROW
   ======================================== */

.schedule-price__schedule-row {
  display: grid;

  grid-template-columns: 1fr 1fr;

  flex: 1;

  /*
   * Горизонтальная линия только
   * между большими группами.
   */
}

.schedule-price__schedule-row + .schedule-price__schedule-row {
  border-top: 2px solid #000000;
}


/* ========================================
   DAYS
   ======================================== */

.schedule-price__days {
  display: flex;
  flex-direction: column;

  justify-content: center;

  border-right: 2px solid #000000;
}


/* ========================================
   DAY
   ======================================== */

.schedule-price__day {
  padding: 8px 10px;

  font-size: 17px;
  font-weight: 400;

  line-height: 1.4;

  text-transform: lowercase;
}


/* ========================================
   TIMES
   ======================================== */

.schedule-price__times {
  display: flex;
  flex-direction: column;

  justify-content: center;
}


/* ========================================
   TIME
   ======================================== */

.schedule-price__time {
  flex: 1;

  display: flex;
  align-items: center;

  padding: 8px 10px;

  font-size: 17px;
  font-weight: 400;

  line-height: 1.4;
}



/* ========================================
   PRICE
   ======================================== */

.schedule-price__prices {
  display: flex;
  flex-direction: column;

  flex: 1;

  /*
   * Растягиваем строки на всю
   * оставшуюся высоту карточки.
   */
}


/* ========================================
   PRICE ROW
   ======================================== */

.schedule-price__price-row {
  display: grid;

  grid-template-columns: 5fr 1fr;

  flex: 1;

  min-height: 0;
}


/*
 * Горизонтальные разделители.
 */

.schedule-price__price-row + .schedule-price__price-row {
  border-top: 2px solid #000000;
}


/* ========================================
   PRICE NAME
   ======================================== */

.schedule-price__price-name {
  display: flex;
  align-items: center;

  padding: 15px 10px;

  border-right: 2px solid #000000;

  font-size: 20px;
  font-weight: 400;

  line-height: 1.4;
}


/* ========================================
   PRICE VALUE
   ======================================== */

.schedule-price__price-value {
  display: flex;
  align-items: center;
  justify-content: center;

  padding: 15px 10px;

  font-size: 20px;
  font-weight: 700;

  line-height: 1.4;
}


/* ========================================
   TABLET
   ======================================== */

@media (max-width: 1000px) {

  .schedule-price {
    padding: 60px 50px;
  }


  .schedule-price__title {
    font-size: 28px;
  }


  .schedule-price__subtitle {
    margin-bottom: 35px;

    font-size: 21px;
  }


  .schedule-price__tables {
    gap: 25px;
  }


  .schedule-price__card {
    padding: 25px;

    border-radius: 25px;
  }


  .schedule-price__card-title {
    font-size: 20px;
  }


  .schedule-price__day,
  .schedule-price__time {
    font-size: 15px;
  }


  .schedule-price__price-name,
  .schedule-price__price-value {
    font-size: 17px;
  }

}


/* ========================================
   MOBILE
   ======================================== */

@media (max-width: 600px) {

  .schedule-price {
    padding: 40px 25px;
  }


  .schedule-price__title {
    font-size: 26px;
  }


  .schedule-price__subtitle {
    margin: 8px 0 30px;

    font-size: 18px;
  }


  .schedule-price__tables {
    grid-template-columns: 1fr;

    gap: 25px;
  }


  .schedule-price__card {
    padding: 22px 18px;

    border-radius: 20px;

    border-width: 4px;
  }


  .schedule-price__card-title {
    font-size: 19px;
  }


  .schedule-price__day,
  .schedule-price__time {
    font-size: 14px;
  }


  .schedule-price__price-row {
    grid-template-columns: 5fr 1fr;
  }


  .schedule-price__price-name,
  .schedule-price__price-value {
    font-size: 15px;
  }

}

</style>