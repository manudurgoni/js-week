<template>
  <header class="MainHeader bg-red-500">
    <div class="MainHeader__container max-w-4xl mx-auto px-4 py-6 bg-red-100 flex">
      <img src="@/assets/logo.svg" alt="Digits logo">

      <nav class=" ml-16">
        <router-link class="link" to="/">Accueil</router-link>
        <router-link class="link" to="/about">À propos</router-link>
      </nav>

      <div class="contact ml-auto ">
        <a href="#" class="link">+00 123 456 789</a>
        <a href="#" class="bg-blue-button">Contact Us</a>
      </div>
    </div>
  </header>
</template>

<style lang="postcss" scoped>
.link {
  @apply mr-10 p-3 text-blue-dark;
}

.link:focus,
.link:hover {
  @apply text-blue-button;
}
</style>