<template>
  <div class="PlayerScroll" >
    <div class="PlayerScroll__video fixed top-0 left-0 h-screen w-screen">
      <video ref="video" class="absolute object-cover w-full h-full" src="/assets/rocket_1.mp4"></video>
    </div>
    <div ref="fake-height" class="PlayerScroll__fake-height absolute top-0 left-0"></div>

    <div class="content absolute top-0 z-10 text-white text-6xl">
      <div class="slide h-screen">
        <h1>Salut</h1>
      </div>
      
      <div class="slide h-screen">
        <h1>Deuxieme</h1>
      </div>
      <div class="slide h-screen">
      </div>
      <div class="slide h-screen">
        <h1>Troisieme</h1>
      </div>
    </div>
    
  </div>
</template>

<script>
export default {
  // La fonction mounted est appelée lorsque le component est prêt.
  mounted() {
    this.addListeners()
    this.onUpdate()
  },
  // La fonction beforeDestroy est appelé juste avant que le component soit détruit. 
  // Une component est détruit quand il n'apparait plus sur la page ou quand son code change avec le hot reload.
  beforeDestroy() {
    this.removeListeners()
  },
  methods: {
    addListeners() {
      window.addEventListener('scroll', this.onScroll)
    },
    removeListeners() {
      window.removeEventListener('scroll', this.onScroll)
    },
    onScroll() {
      const scrollY = window.scrollY
      const progressY = scrollY / (window.innerHeight * 4)

      this.currentTime = progressY * this.$refs.video.duration
    },
    onUpdate() {
      this.$refs.video.currentTime = this.currentTime || 0

      requestAnimationFrame(this.onUpdate)
    }
  }
}
</script>

<style lang="postcss" scoped>
.PlayerScroll__fake-height {
  height: 500vh;
  width: 120px;
}
</style>