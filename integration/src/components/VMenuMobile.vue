<template>
  <div class="MenuMobile absolute w-full bg-pink-700">
    <nav class="ml-16 flex flex-col justify-around items-center h-full">
      <router-link class="link" to="/">Accueil</router-link>
      <a class="link"  href="#">Articles</a>
      <a class="link"  href="#">Portfolio</a>
      <router-link class="link" to="/about">À propos</router-link>
    </nav>
  </div>
</template>

<style lang="postcss" scoped>
.MenuMobile {
  top: 72px;
  height: calc(100vh - 72px);
}
</style>