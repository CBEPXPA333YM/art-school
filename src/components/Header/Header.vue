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

        <a href="#works">
          Примеры работ
        </a>

        <a href="#schedule">
          Расписание
        </a>

        <a href="#schedule">
          Стоимость
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
</style>