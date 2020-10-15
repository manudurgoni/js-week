<template>
  <header class="MainHeader fixed top-0 w-full z-10 bg-white">
    <div class="MainHeader__container container py-4 flex items-center">
      <img src="@/assets/logo.svg" alt="Digits logo">

      <nav class=" ml-16 hidden md:block">
        <router-link class="link" to="/">Accueil</router-link>
        <router-link class="link" to="/about">À propos</router-link>
      </nav>

      <div class="contact ml-auto items-center hidden md:flex">
        <a href="#" class="link">+00 123 456 789</a>
        <a href="#" class="link-rounded">Contact Us</a>
      </div>

      <button ref="button" class="ml-auto menu-btn" :class="{ 'menu-btn--open': isMenuOpen }" @click="toggleMenu">
        <span class="bar"></span>
        <span class="bar"></span>
        <span class="bar"></span>

        <span class="sr-only">Menu</span>
      </button>
    </div>
    <v-menu-mobile v-show="isMenuOpen"></v-menu-mobile>
  </header>
</template>

<script>
import VMenuMobile from '@/components/VMenuMobile'
export default {
  watch:{
    $route (){
      this.isMenuOpen = false
    }
  },
  components: {
    VMenuMobile
  },
  data() {
    return {
      isMenuOpen: false
    }
  },
  methods: {
    toggleMenu() {
      console.log('menu')
      this.isMenuOpen = !this.isMenuOpen
    }
  }
}
</script>

<style lang="postcss" scoped>
.menu-btn {
  width: 40px;
  height: 40px;
  outline: none;
  padding: 13px 10px;
  @apply border-blue-button border flex flex-col justify-between rounded-full transition duration-500;
}

@screen md {
  .menu-btn {
    display: none;
  }
}

.menu-btn .bar {
  width: 18px;
  height: 2px;
  @apply bg-blue-button block transition duration-500 origin-center;
}

.menu-btn:focus,
.menu-btn:hover {
  @apply  bg-blue-button;
}

@media (hover: none) {
  .menu-btn:hover { color: inherit; }
}

.menu-btn:focus .bar,
.menu-btn:hover .bar {
  @apply bg-white;
}

/**
  Menu open
 */

.menu-btn--open .bar:nth-child(1){
  transform: translateY(5px) rotate(45deg);
}

.menu-btn--open .bar:nth-child(2){
  transform: scaleX(0);
}

.menu-btn--open .bar:nth-child(3){
  transform: translateY(-5px) rotate(-45deg);
}

</style>