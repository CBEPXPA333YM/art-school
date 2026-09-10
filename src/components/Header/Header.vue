<template>
  <header class="header">
    <div class="container header__inner">

      <nav class="header__nav">

        <a href="#about">
          О студии
        </a>

        <a href="#program">
          Программа обучения
        </a>

        <a href="#schedule">
          Расписание
        </a>

        <a href="#works">
          Примеры работ
        </a>

        <a href="#schedule">
          Стоимость
        </a>

        <a href="#contacts">
          Адрес
        </a>

      </nav>

    </div>
  </header>
</template>


<style lang="scss" scoped>
@use '../../assets/styles/variables' as *;


.header {
  width: 100%;

  padding: 24px 0;

  background-color: $color-background;
}


.header__inner {
  display: flex;

  align-items: center;
  justify-content: space-between;

  gap: 40px;
}


.header__nav {
  display: flex;

  align-items: center;

  /*
   * Кнопки занимают всю ширину
   */

  width: 100%;

  font-size: 15px;
  font-weight: 700;
}


.header__nav a {
  flex: 1;

  text-align: center;

  transition: opacity $transition-fast;

  &:hover {
    opacity: 0.6;
  }
}


@media (max-width: 600px) {

  .header {
    padding: 16px 0;
  }


  .header__inner {
    gap: 0;
  }


  .header__nav {
    display: grid;

    grid-template-columns: repeat(2, 1fr);

    grid-template-rows: repeat(3, auto);

    width: 100%;

    row-gap: 14px;

    column-gap: 0px;

    font-size: 13px;
  }


  .header__nav a {
    flex: none;

    text-align: left;
  }

  .header__nav a:nth-child(even) {
    transform: translateX(-50px);
  }

}
</style>