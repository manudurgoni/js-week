<template>
  <div id="app" class="open-sans">
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
