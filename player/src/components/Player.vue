<template>
  <div class="Player max-w-full mx-6 md:mx-12 lg:mx-auto lg:max-w-5xl relative">
    <video @timeupdate="onUpdate" class="w-full" src="/assets/video.mp4" controls=true muted></video>

    <div class="Player__layer absolute top-0 left-0 w-full h-full text-left pointer-events-none p-12 text-white">
      <h1 class=" text-4xl font-bold">Mon texte</h1>
    </div>
  </div>
</template>

<script>
import data from '@/assets/data.json'
export default {
  mounted() {
    console.log(data)
    // const video = this.$el.querySelector('video')
    // video.addEventListener('timeupdate', this.onUpdate)
  },
  methods: {
    onUpdate(e) {
      const video = e.target
      const currentTime = video.currentTime
      console.log(currentTime)
    }
  }
}
</script>

<style lang="postcss" scoped>
/**
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
 */
</style>