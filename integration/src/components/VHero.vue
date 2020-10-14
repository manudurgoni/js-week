<template>
  <div class="Hero text-center">
    <div class="Hero__container container pt-20">
      <h1 class="title text-blue-dark" data-scroll data-scroll-speed="2">Good design meets<br>great user experience</h1>
      <p class="my-6 text-blue-text text-lg">For everyone, from beginners to experts</p>

      <div class="buttons">
        <a href="#" class="link-rounded mx-3">Buy Digits</a>
        <a href="#" class="link-rounded link-rounded--white mx-3">See the Features</a>
      </div>

      <div class="illustration mt-24">
        <v-illustration class="w-full h-auto"></v-illustration>
      </div>
    </div>
  </div>
</template>

<script>
import VIllustration from '@/components/VIllustration'
export default {
  components: {
    VIllustration
  }
}
</script>

<style lang="postcss" scoped>
.Hero {
  position: relative;
}

.Hero::before {
  content: '';
  display: block;
  height: 80%;
  width: 100%;
  background: linear-gradient(180deg, rgba(242, 249, 255, 0.12) 0%, #F2F9FF 100%);
  position: absolute;
  top: 0;
  left: 0;
  z-index: -1;
}

.title {
  @apply text-blue-dark font-bold leading-none;
  font-size: 32px;
}

@screen md {
  .title {
    font-size: 56px;
  }
}

</style>