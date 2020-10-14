<template>
  <header class="MainHeader">
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
    </div>
  </header>
</template>