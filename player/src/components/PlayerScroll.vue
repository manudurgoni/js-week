<template>
  <div class="PlayerScroll">
    <div class="PlayerScroll__video fixed top-0 left-0 h-screen w-screen">
      <video class="absolute object-cover w-full h-full" src="/assets/rocket.mp4"></video>
    </div>
    <div class="PlayerScroll__fake-height absolute"></div>
  </div>
</template>

<style lang="postcss" scoped>
.PlayerScroll__fake-height {
  height: 5000px;
  width: 1px;
}
</style>