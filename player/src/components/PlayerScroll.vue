<template>
  <div class="PlayerScroll" >
    <div class="PlayerScroll__video fixed top-0 left-0 h-screen w-screen">
      <video class="absolute object-cover w-full h-full" src="/assets/rocket.mp4"></video>
    </div>
    <div class="PlayerScroll__fake-height absolute top-0 left-0"></div>
  </div>
</template>

<script>
export default {
  // La fonction mounted est appelée lorsque le component est prêt.
  mounted() {
    this.addListeners()
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
    onScroll: () => {
      const scrollY = window.scrollY
      console.log(scrollY)
    }
  }
}
</script>

<style lang="postcss" scoped>
.PlayerScroll__fake-height {
  height: 5000px;
  width: 120px;
  background: linear-gradient(to bottom, red, #000);
}
</style>