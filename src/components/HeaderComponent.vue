<template lang='pug'>
div.container.header-container
  div.header__top-part
    a(href='/').header__logo
    form.header__form
      input(type="text", id="search").header__input
      button(type="submit").header__btn Поиск
  button.header__btn-burger(@click="show = !show")
  nav.header__nav(:class="{'header__nav--opacity': !show}")
    ul.header__list
      li.header__item
        a(href="").header__link Аукционные каталоги
      li.header__item
        a(href="").header__link Коллекционирование
      li.header__item
        a(href="").header__link Колоbook
      li.header__item
        a(href="").header__link Разное
      li.header__item
        a(href="").header__link Авторы
      li.header__item
        a(href="").header__link Контакты

</template>


<script>
export default {
  name: 'HeaderComponent',
    
    data() {
        return {
            show: false,
        }
    },
    
}
</script>

<style lang="scss">

@import "../assets/scss/general.scss";

.header-container {
  padding-top: 25px;
}

.header__logo {
  display: block;
  width: 340px;
  height: 81px;
  background: transparent url('../assets/logo.png') no-repeat center;
}

</style>
