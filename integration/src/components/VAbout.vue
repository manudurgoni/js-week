<template>
  <div class="About">
    <div class="About__container max-w-6xl mx-auto pt-20 pb-48">
      <h2 class="title">Whatever work you do,<br>we're able to help</h2>

      <div class="flex justify-between mt-16">
        <div class="About__imgs">
          <img src="@/assets/img/girl-1.png" alt="">
          <img src="@/assets/img/guy-1.png" alt="">
          <img src="@/assets/img/guy-2.png" alt="">
        </div>

        <div class="About__features mt-20">
          <div class="feature">
            <img src="@/assets/svg/icon-1.svg" alt="" class="feature__icon">
            <div class="feature__content">
              <h3>Design and Assets</h3>
              <p>Make your brand stand out with pixel-perfect design crafted to perfection.</p>
            </div>
          </div>

          <div class="feature">
            <img src="@/assets/svg/icon-2.svg" alt="" class="feature__icon">
            <div class="feature__content">
              <h3>Easy Content</h3>
              <p>Import your demos or build pages visually. Bonus: All images and illustrations included!</p>
            </div>
          </div>

          <div class="feature">
            <img src="@/assets/svg/icon-3.svg" alt="" class="feature__icon">
            <div class="feature__content">
              <h3>Fast and Reliable</h3>
              <p>No heavy-weight plugins. No builders. No unneccesary file loading. Pure WordPress.</p>
            </div>
          </div>
        </div>
      </div>

    </div>
  </div>
</template>

<style lang="postcss" scoped>
.title {
  @apply text-blue-dark font-bold leading-none text-center;
  font-size: 48px;
}

/*
  Imgs
*/
.About__imgs img:nth-child(1) {
  margin-left: 180px;
}
.About__imgs img:nth-child(2) {
  margin-top: -94px;
}
.About__imgs img:nth-child(3) {
  margin-top: -142px;
  margin-left: 200px;
}

/** 
  Features
 */
.About__features {
  max-width: 405px;
}

.About__features .feature {
  @apply flex items-start border-b border-blue-text border-opacity-25 mb-12 pb-12;
}

.About__features .feature:last-child {
  @apply border-none;
}

.feature .feature__content {
  @apply ml-12 border-black;
}

.feature .feature__content h3 {
  @apply font-bold text-xl text-blue-dark mb-6 leading-none;
}

.feature .feature__content p {
  @apply text-lg text-blue-text leading-relaxed;
}
</style>