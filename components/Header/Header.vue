<template>
  <header class="header">
    <a href="/">
      <img class="header__img" src="/img/Bookd.svg" alt="logo" />
    </a>

    <nav>
      <Burger class="burger-menu" :isActive="menuOpen" :onClick="toggleMenu" />

      <ul class="nav" :class="{ 'nav--open': menuOpen }">
        <li class="nav__link">
          <a href="/" @click="closeMenu">Ana sayfa</a>
        </li>
        <li class="nav__link">
          <a href="#about" @click="closeMenu">Hakkımızda</a>
        </li>
        <li class="nav__link">
          <a href="#author" @click="closeMenu">Temas etmek</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
import { ref } from 'vue';
import Burger from '~/components/icon/Burger.vue';

export default {
  components: {
    Burger,
  },
  setup() {
    const menuOpen = ref(false);

    const toggleMenu = () => {
      menuOpen.value = !menuOpen.value;
      console.log('Menu open:', menuOpen.value);
    };

    const closeMenu = () => {
      menuOpen.value = false;
    };

    return {
      menuOpen,
      toggleMenu,
      closeMenu,
    };
  },
};
</script>

<style>
.header {
  padding: 30px 5%;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.burger-menu {
  cursor: pointer;
  display: block;
}

.nav {
  display: none;
  flex-direction: column;
  position: fixed;
  top: 0;
  left: 0;
  height: 100%;
  background-color: rgba(255, 255, 255, 0.95);
  width: 250px;
  box-shadow: 2px 0 5px rgba(0, 0, 0, 0.2);
  z-index: 1000;
  transform: translateX(-100%);
  transition: transform 0.3s ease-in-out;
}

.nav.nav--open {
  transform: translateX(0);
  display: flex;
  background-color: #14452f;
  padding-top: 30px;
}

.nav.nav--open .nav__link {
  color: #fff;
}

.nav__link {
  color: #232323;
  font-family: inherit;
  font-size: 15px;
  font-style: normal;
  font-weight: 400;
  line-height: 22.5px;
  text-transform: uppercase;
  padding: 15px;
  width: 100%;
  text-align: center;
}

@media (min-width: 900px) {
  .burger-menu {
    display: none;
  }

  .nav {
    display: flex;
    flex-direction: row;
    position: static;
    height: auto;
    background-color: transparent;
    width: auto;
    box-shadow: none;
    transform: none;
  }

  .nav__link {
    padding: 0 15px;
    width: auto;
    text-align: left;
  }
}
</style>
