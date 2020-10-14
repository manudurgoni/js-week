<template>
  <div id="app" class="open-sans pt-20">
    <v-header></v-header>
    <router-view/>
  </div>
</template>

<script>
import VHeader from '@/components/VHeader'
export default {
  components: {
    VHeader
  }
}
</script>

<style>
</style>
