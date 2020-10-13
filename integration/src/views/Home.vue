<template>
  <div class="home">
    <v-hero></v-hero>
    <v-about></v-about>
  </div>
</template>

<script>
import VHero from '@/components/VHero'
import VAbout from '@/components/VAbout'
export default {
  name: 'Home',
  components: {
    VHero,
    VAbout
  }
}
</script>
