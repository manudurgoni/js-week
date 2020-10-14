<template>
  <div id="app" class="open-sans" data-scroll-container>
    <v-header></v-header>
    <router-view/>
  </div>
</template>

<script>
import LocomotiveScroll from 'locomotive-scroll'
import VHeader from '@/components/VHeader'
export default {
  components: {
    VHeader
  },
  mounted() {
    this.scroll = new LocomotiveScroll({
      el: this.$el,
      smooth: true
    })
  }
}
</script>

<style>
</style>
