<template>
  <header class="MainHeader">
    <div class="MainHeader__container max-w-6xl mx-auto px-4 py-4 flex items-center">
      <img src="@/assets/logo.svg" alt="Digits logo">

      <nav class=" ml-16">
        <router-link class="link" to="/">Accueil</router-link>
        <router-link class="link" to="/about">À propos</router-link>
      </nav>

      <div class="contact ml-auto flex  items-center  ">
        <a href="#" class="link">+00 123 456 789</a>
        <a href="#" class="link-rounded">Contact Us</a>
      </div>
    </div>
  </header>
</template>