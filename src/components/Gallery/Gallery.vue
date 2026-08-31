<script setup lang="ts">

import { ref, computed } from 'vue'
import image1 from '../../assets/images/gallery/1.png'
import image2 from '../../assets/images/gallery/2.png'
import image3 from '../../assets/images/gallery/3.png'
import image4 from '../../assets/images/gallery/4.png'


const images = [
  {
    src: image1,
    alt: 'Работа выполнена акварелью'
  },

  {
    src: image2,
    alt: 'Работа выполнена гуашью'
  },

  {
    src: image3,
    alt: 'Работа выполнена карандашами'
  },

  {
    src: image4,
    alt: 'Работа выполнена фломастерами'
  }
]

const currentIndex = ref(0)


/* ========================================
   PREVIOUS
   ======================================== */

function previous() {
  currentIndex.value =
    (currentIndex.value - 1 + images.length) % images.length
}


/* ========================================
   NEXT
   ======================================== */

function next() {
  currentIndex.value =
    (currentIndex.value + 1) % images.length
}


/* ========================================
   CURRENT IMAGE
   ======================================== */

const currentImage = computed(() => {
  return images[currentIndex.value]
})


/* ========================================
   PREVIOUS IMAGE
   ======================================== */

const previousImage = computed(() => {
  const index =
    (currentIndex.value - 1 + images.length) % images.length

  return images[index]
})


/* ========================================
   NEXT IMAGE
   ======================================== */

const nextImage = computed(() => {
  const index =
    (currentIndex.value + 1) % images.length

  return images[index]
})

</script>


<template>

  <section id="works" class="gallery">

    <!-- ========================================
         TITLE
         ======================================== -->

    <h2 class="gallery__title">
      ПРИМЕРЫ РАБОТ
    </h2>


    <!-- ========================================
         CAROUSEL
         ======================================== -->

    <div class="gallery__carousel">


      <!-- ======================================
           PREVIOUS BUTTON
           ====================================== -->

      <button
        class="gallery__arrow gallery__arrow--left"
        type="button"
        aria-label="Предыдущая работа"
        @click="previous"
      >
        ←
      </button>


      <!-- ======================================
           PREVIOUS PREVIEW
           ====================================== -->

      <div
        class="gallery__preview gallery__preview--left"
        @click="previous"
      >

        <img
          :src="previousImage.src"
          :alt="previousImage.alt"
        >

      </div>


      <!-- ======================================
           CURRENT IMAGE
           ====================================== -->

      <div class="gallery__current">

        <img
          :src="currentImage.src"
          :alt="currentImage.alt"
        >

      </div>


      <!-- ======================================
           NEXT PREVIEW
           ====================================== -->

      <div
        class="gallery__preview gallery__preview--right"
        @click="next"
      >

        <img
          :src="nextImage.src"
          :alt="nextImage.alt"
        >

      </div>


      <!-- ======================================
           NEXT BUTTON
           ====================================== -->

      <button
        class="gallery__arrow gallery__arrow--right"
        type="button"
        aria-label="Следующая работа"
        @click="next"
      >
        →
      </button>

    </div>

  </section>

</template>


<style lang="scss" scoped>

/* ========================================
   GALLERY
   ======================================== */

.gallery {
  width: 100%;

  padding: 80px;

  background-color: #ffffff;

  overflow: hidden;
}


/* ========================================
   TITLE
   ======================================== */

.gallery__title {
  margin: 0 0 60px;

  color: #d71920;

  font-size: 32px;
  font-weight: 700;
  line-height: 1.1;
}


/* ========================================
   CAROUSEL
   ======================================== */

.gallery__carousel {
  position: relative;

  display: flex;

  align-items: center;
  justify-content: center;

  width: 100%;
  min-height: 500px;

  gap: 30px;
}


/* ========================================
   CURRENT IMAGE
   ======================================== */

.gallery__current {
  position: relative;

  z-index: 2;

  display: flex;

  align-items: center;
  justify-content: center;

  width: min(50%, 600px);

  flex-shrink: 0;
}


.gallery__current img {
  display: block;

  width: 100%;
  height: auto;

  object-fit: contain;
}


/* ========================================
   PREVIEWS
   ======================================== */

.gallery__preview {
  position: relative;

  z-index: 1;

  display: flex;

  align-items: center;
  justify-content: center;

  width: min(20%, 240px);

  flex-shrink: 0;

  cursor: pointer;

  opacity: 0.45;

  transform: scale(0.8);

  transition:
    opacity 0.25s ease,
    transform 0.25s ease;
}


.gallery__preview:hover {
  opacity: 0.7;

  transform: scale(0.85);
}


.gallery__preview img {
  display: block;

  width: 100%;
  height: auto;

  object-fit: contain;
}


/* ========================================
   ARROWS
   ======================================== */

.gallery__arrow {
  position: absolute;

  top: 50%;

  z-index: 3;

  display: flex;

  align-items: center;
  justify-content: center;

  width: 50px;
  height: 50px;

  padding: 0;

  border: none;

  background: transparent;

  color: #000000;

  font-size: 42px;
  line-height: 1;

  cursor: pointer;

  transform: translateY(-50%);

  transition:
    opacity 0.2s ease,
    transform 0.2s ease;
}


.gallery__arrow:hover {
  opacity: 0.6;
}


.gallery__arrow--left {
  left: 0;
}


.gallery__arrow--right {
  right: 0;
}


/* ========================================
   TABLET
   ======================================== */

@media (max-width: 1000px) {

  .gallery {
    padding: 60px 50px;
  }


  .gallery__title {
    margin-bottom: 50px;

    font-size: 28px;
  }


  .gallery__carousel {
    min-height: 400px;

    gap: 20px;
  }


  .gallery__current {
    width: 50%;
  }


  .gallery__preview {
    width: 20%;
  }


  .gallery__arrow {
    width: 40px;
    height: 40px;

    font-size: 34px;
  }

}


/* ========================================
   MOBILE
   ======================================== */

@media (max-width: 600px) {

  .gallery {
    padding: 40px 25px;
  }


  .gallery__title {
    margin-bottom: 40px;

    font-size: 26px;
  }


  .gallery__carousel {
    min-height: 300px;

    gap: 8px;
  }


  /* ======================================
     CURRENT
     ====================================== */

  .gallery__current {
    width: 58%;
  }


  /* ======================================
     PREVIEWS
     ====================================== */

  .gallery__preview {
    width: 20%;

    opacity: 0.35;

    transform: scale(0.75);
  }


  .gallery__preview:hover {
    opacity: 0.5;

    transform: scale(0.8);
  }


  /* ======================================
     ARROWS
     ====================================== */

  .gallery__arrow {
    width: 35px;
    height: 35px;

    font-size: 28px;
  }


  .gallery__arrow--left {
    left: -5px;
  }


  .gallery__arrow--right {
    right: -5px;
  }

}

</style>