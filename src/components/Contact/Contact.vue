
<script setup lang="ts">

import {
  onMounted,
  onBeforeUnmount,
  ref
} from 'vue'


/* ========================================
   YANDEX MAP
   ======================================== */

const mapElement =
  ref<HTMLElement | null>(null)

let map: any = null


/* ========================================
   КООРДИНАТЫ СТУДИИ
   ======================================== */

const studioCoordinates = [
  37.778604,
  55.939408
]


/* ========================================
   LOAD YANDEX MAPS
   ======================================== */

async function loadYandexMaps() {

  const apiKey =
    import.meta.env.VITE_YANDEX_MAPS_API_KEY


  if (!apiKey) {

    console.error(
      'Не найден VITE_YANDEX_MAPS_API_KEY'
    )

    return
  }


  /* ----------------------------------------
     Если API уже загружен
     ---------------------------------------- */

  if ((window as any).ymaps3) {

    await initMap()

    return
  }


  /* ----------------------------------------
     Создаем script
     ---------------------------------------- */

  const script =
    document.createElement('script')


  script.src =
    `https://api-maps.yandex.ru/v3/?apikey=${apiKey}&lang=ru_RU`

  script.type =
    'text/javascript'


  /* ----------------------------------------
     Ждем загрузку
     ---------------------------------------- */

  await new Promise<void>((resolve, reject) => {

    script.onload = () => resolve()


    script.onerror = () => reject(
      new Error(
        'Не удалось загрузить Yandex Maps API'
      )
    )


    document.head.appendChild(script)

  })


  await initMap()

}


/* ========================================
   INITIALIZE MAP
   ======================================== */

async function initMap() {

  if (!mapElement.value) {
    return
  }


  const ymaps3 =
    (window as any).ymaps3


  if (!ymaps3) {

    console.error(
      'Yandex Maps API не загружен'
    )

    return
  }


  await ymaps3.ready


  const {
    YMap,
    YMapDefaultSchemeLayer,
    YMapDefaultFeaturesLayer,
    YMapMarker
  } = ymaps3


  /* ----------------------------------------
     Создаем карту
     ---------------------------------------- */

  map = new YMap(
    mapElement.value,
    {
      location: {
        center: studioCoordinates,

        zoom: 16
      }
    }
  )


  /* ----------------------------------------
     Основной слой карты
     ---------------------------------------- */

  map.addChild(
    new YMapDefaultSchemeLayer()
  )


  /* ----------------------------------------
     Слой объектов
     ---------------------------------------- */

  map.addChild(
    new YMapDefaultFeaturesLayer()
  )


  /* ========================================
     МЕТКА СТУДИИ
     ======================================== */

  if (!YMapMarker) {

    console.error(
      'YMapMarker недоступен'
    )

    return
  }


  /* ----------------------------------------
     HTML метки
     ---------------------------------------- */

  const markerElement =
    document.createElement('div')


  markerElement.innerHTML = `
    <div
      style="
        position: relative;
        width: 36px;
        height: 36px;
        background: #d71920;
        border: 4px solid #ffffff;
        border-radius: 50% 50% 50% 0;
        box-sizing: border-box;
        transform: rotate(-45deg);
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.4);
      "
    >

      <div
        style="
          position: absolute;
          top: 50%;
          left: 50%;
          width: 10px;
          height: 10px;
          background: #ffffff;
          border-radius: 50%;
          transform: translate(-50%, -50%);
        "
      ></div>

    </div>
  `


  /* ----------------------------------------
     Размер и положение контейнера
     ---------------------------------------- */

  markerElement.style.width = '36px'

  markerElement.style.height = '36px'

  markerElement.style.transform =
    'translate(-50%, -100%)'


  /* ----------------------------------------
     Создаем маркер
     ---------------------------------------- */

  const marker =
    new YMapMarker(
      {
        coordinates:
          studioCoordinates
      },
      markerElement
    )


  /* ----------------------------------------
     Добавляем маркер
     ---------------------------------------- */

  map.addChild(marker)

}


/* ========================================
   MOUNT
   ======================================== */

onMounted(() => {

  loadYandexMaps()
    .catch(error => {

      console.error(
        'Ошибка загрузки Яндекс Карт:',
        error
      )

    })

})


/* ========================================
   UNMOUNT
   ======================================== */

onBeforeUnmount(() => {

  if (map) {

    map.destroy()

    map = null

  }

})

</script>


<template>

  <section
    id="contacts"
    class="contacts"
  >

    <div class="contacts__content">


      <!-- ==================================
           ЗАГОЛОВОК
           ================================== -->

      <h2 class="contacts__title">
        АДРЕС СТУДИИ И КОНТАКТЫ
      </h2>


      <!-- ==================================
           СОЦИАЛЬНЫЕ СЕТИ
           ================================== -->

<div class="contacts__socials">

  <a
    href="https://vk.ru/sverhra333um"
    class="contacts__social"
    aria-label="MAX"
  >
    <img
      src="../../assets/images/hero/social/max_pict.png"
      alt="MAX"
    >
  </a>


  <a
    href="https://vk.ru/sverhra333um"
    class="contacts__social"
    aria-label="VK"
  >
    <img
      src="../../assets/images/hero/social/vk_pict.png"
      alt="VK"
    >
  </a>

</div>




      <!-- ==================================
           ТЕЛЕФОН
           ================================== -->

      <a
        href="tel:+79104697054"
        class="contacts__phone"
      >
        Тел.: +7 910 460 7054
      </a>


      <!-- ==================================
           АДРЕС
           ================================== -->

      <address class="contacts__address">

        Адрес: Библиотека №3<br>

        Московская область<br>

        г. Мытищи, ул. Силикатная, д. 37<br>

        тел.: +7 910 469 7054<br>

        <span class="contacts__second-phone">
          +7 (495) 583 7 34 1
        </span><br>

        mail: lsbigwings@gmail.com<br>

        <span class="contacts__second-phone">
          biblioteka_3@mail.ru
        </span><br>

      </address>

    </div>


    <!-- ==================================
         ЯНДЕКС КАРТА
         ================================== -->

    <div class="contacts__map-wrapper">

      <div
        ref="mapElement"
        class="contacts__map"
      ></div>

    </div>

  </section>

</template>


<style lang="scss" scoped>


/* ========================================
   CONTACTS
   ======================================== */

.contacts {
  display: grid;

  grid-template-columns: 1fr 1fr;

  width: 100%;

  height: 600px;

  background-color: #eeedee;
}


/* ========================================
   CONTENT
   ======================================== */

.contacts__content {
  display: flex;

  flex-direction: column;

  align-items: center;
  text-align: center;

  justify-content: center;

  padding: 80px;

  box-sizing: border-box;

}


/* ========================================
   TITLE
   ======================================== */

.contacts__title {
  margin: 0 0 30px;

  color: #d71920;

  font-size: 36px;

  font-weight: 700;

  line-height: 1.1;
}


/* ========================================
   SOCIALS
   ======================================== */

.contacts__socials {
  display: flex;
  align-self: center;
  align-items: center;

  gap: 14px;

  margin-bottom: 24px;
}


.contacts__social {
  display: flex;

  align-items: center;

  justify-content: center;

  width: 40px;

  height: 40px;
}


.contacts__social img {
  display: block;

  width: 100%;

  height: 100%;

  object-fit: contain;
}


/* ========================================
   PHONE
   ======================================== */

.contacts__phone {
  display: block;

  color: #000000;

  font-size: 24px;

  font-weight: 600;

  line-height: 1.3;

  text-decoration: none;

  transition: opacity 0.2s ease;
}


.contacts__phone:hover {
  opacity: 0.6;
}


/* ========================================
   ADDRESS
   ======================================== */

.contacts__address {
  margin: 14px 0 0;

  color: #000000;

  font-size: 18px;

  font-weight: 400;

  line-height: 1.4;

  font-style: normal;

  text-align: left;
}


.contacts__second-phone {
  display: inline-block;

  margin-left: 44px;
}


/* ========================================
   MAP WRAPPER
   ======================================== */

.contacts__map-wrapper {
  position: relative;

  width: 100%;

  height: 600px;

  overflow: hidden;
}


/* ========================================
   MAP
   ======================================== */

.contacts__map {
  width: 100%;

  height: 100%;

  overflow: hidden;
}


/* ========================================
   TABLET
   ======================================== */

@media (max-width: 1000px) {

  .contacts {
    height: 500px;
  }


  .contacts__content {
    padding: 50px;
  }


  .contacts__title {
    font-size: 30px;
  }


  .contacts__social {
    width: 34px;

    height: 34px;
  }


  .contacts__phone {
    font-size: 20px;
  }


  .contacts__address {
    font-size: 16px;
  }


  .contacts__map-wrapper {
    height: 500px;
  }

}


/* ========================================
   MOBILE
   ======================================== */

@media (max-width: 600px) {

  .contacts {
    display: flex;

    flex-direction: column;

    height: auto;

    min-height: 0;
  }


  .contacts__content {
    order: 1;

    width: 100%;

    padding: 50px 25px;

    align-items: center;

    text-align: center;
  }


  .contacts__title {
    margin-bottom: 20px;

    font-size: 24px;

    line-height: 1.1;

    text-align: center;
  }


  .contacts__socials {
    gap: 8px;

    margin-bottom: 18px;
  }


  .contacts__social {
    width: 30px;

    height: 30px;
  }


  .contacts__phone {
    font-size: 18px;
  }


  .contacts__address {
    margin-top: 10px;

    font-size: 14px;

    line-height: 1.4;

    text-align: center;
  }


  .contacts__second-phone {
    margin-left: 0;
  }


  .contacts__map-wrapper {
    order: 2;

    width: 100%;

    height: 400px;
  }


  .contacts__map {
    width: 100%;

    height: 400px;
  }

}

</style>

