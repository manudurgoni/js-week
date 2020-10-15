<template>
  <div class="Hero text-center">
    <div class="Hero__container container pt-20">
      <h1 ref="title" class="title text-blue-dark">Good design meets<br>great user experience</h1>
      <p ref="baseline" class="my-6 text-blue-text text-lg">For everyone, from beginners to experts</p>

      <div ref="buttons" class="buttons">
        <a href="#" class="link-rounded mx-3">Buy Digits</a>
        <a href="#" class="link-rounded link-rounded--white mx-3">See the Features</a>
      </div>

      <div ref="illustration" class="illustration mt-24">
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
    const tl = gsap.timeline({
      delay: 1
    })

    // tl.timeScale(2)

    /**
     * Animation du title
     */
    const title = this.$refs.title
    const chars = Splitting({ target: title, by: 'chars' })[0].chars
    tl.from(chars, {
      delay: 1,
      autoAlpha: 0,
      scaleY: 0,
      y: (i) => {
        return (chars.length - Math.cos(1 + i))
      },
      x: 0,
      stagger: 0.03,
      ease: "elastic.out(2, 0.8)",
      duration: 0.85
    }, 'start')

    /**
     * Animation de la baseline
     */
    tl.from(this.$refs.baseline, {
      y: 20,
      autoAlpha: 0,
      ease: "expo.out",
      duration: 0.8
    }, 'start+=2.2')
    
    /**
     * Animation des boutons
     */
    tl.from(this.$refs.buttons.querySelectorAll('a'), {
      y: 20,
      autoAlpha: 0,
      stagger: 0.1,
      ease: "elastic.out(1, 2.8)",
      duration: 0.8
    })
    
    /**
     * Animation illustation
     */
    tl.from(this.$refs.illustration, {
      y: 50,
      scale: 1.1,
      autoAlpha: 0,
      stagger: 0.1,
      ease: "sine.out",
      duration: 0.8
    }, '-=0.6')
  }
}
</script>

<style lang="postcss" scoped>
>>> .char {
  display: inline-block;
}

.Hero {
  position: relative;
  overflow: hidden;
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