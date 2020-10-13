<template>
  <div class="Hero text-center">
    <div class="Hero__container max-w-4xl mx-auto pt-20">
      <h1 class="title text-blue-dark">Good design meets<br>great user experience</h1>
      <p class="my-6 text-blue-text text-lg">For everyone, from beginners to experts</p>

      <div class="buttons">
        <a href="#" class="link-rounded mx-3">Buy Digits</a>
        <a href="#" class="link-rounded link-rounded--white mx-3">See the Features</a>
      </div>

      <div class="illustration mt-24">
        <img src="@/assets/illustration.svg" alt="Jeune femme qui tient un téléphone les cheveux au vent.">
      </div>
    </div>
  </div>
</template>

<style lang="postcss" scoped>
.title {
  @apply text-blue-dark font-bold leading-none;
  font-size: 56px;
}
</style>