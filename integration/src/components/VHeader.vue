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

      <button class="ml-auto menu-btn" @click="toggleMenu">
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
  @apply border-blue-button border flex flex-col justify-between rounded-full;
}

@screen md {
  .menu-btn {
    display: none;
  }
}

.menu-btn .bar {
  width: 100%;
  height: 2px;
  @apply bg-blue-button block;
}

.menu-btn:focus,
.menu-btn:hover {
  @apply  bg-blue-button;
}

.menu-btn:focus .bar,
.menu-btn:hover .bar {
  @apply bg-white;
}



</style>