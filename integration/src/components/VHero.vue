<template>
  <div class="Hero text-center">
    <div class="Hero__container container pt-20">
      <h1 ref="title" class="title text-blue-dark">Good design meets<br>great user experience</h1>
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
import gsap from 'gsap'
import Splitting from 'splitting'

import VIllustration from '@/components/VIllustration'
export default {
  components: {
    VIllustration
  },
  mounted() {
    const title = this.$refs.title
    const chars = Splitting({ target: title, by: 'chars' })[0].chars

    gsap.from(chars, {
      delay: 1,
      autoAlpha: 0,
      y: 30,
      stagger: 0.06,
      // ease: 
      duration: 0.8
    })
  }
}
</script>

<style lang="postcss" scoped>
>>> .char {
  display: inline-block;
}

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