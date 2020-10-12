<template>
  <div class="Player">
    <video src="/assets/cest_bien_nils_.mp4" controls=true muted></video>
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

.Player video {
  width: 100%;
}

@media (min-width: 768px) {
  .Player {
    margin: 0px 40px;
    opacity: 0.6;
  }
}

@media (min-width: 1024px) {
  .Player {
    margin: 0px auto;
    max-width: 900px;
    opacity: 1;
  }
}
</style>