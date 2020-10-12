<template>
  <div class="Player">
    <video src="/assets/video.mp4" controls=true muted></video>
  </div>
</template>

<script>
export default {
  
}
</script>

<style lang="postcss" scoped>
.Player {
  max-width: 100%;
  margin: 0px 24px;
}

@media (min-width: 768px) {
  .Player {
    margin: 0px 40px;
  }
}
</style>