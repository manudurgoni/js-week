<template>
  <div class="About">
    <div class="About__container container pt-20 pb-48">
      <h2 class="title">Whatever work you do,<br class="hidden lg:block">we're able to help</h2>

      <div class="md:flex justify-between mt-16">
        <div class="About__imgs flex-1 md:mr-8">
          <img src="@/assets/img/girl-1.png" alt="">
          <img src="@/assets/img/guy-1.png" alt="">
          <img src="@/assets/img/guy-2.png" alt="">
        </div>

        <div class="About__features mt-20 flex-1">
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
  @apply text-blue-dark font-bold leading-9 text-center;
  font-size: 30px;
}


@screen md {
  .title {
    font-size: 48px;
    line-height: 56px;
  }
}

/*
  Imgs
*/
.About__imgs img:nth-child(1) {
  margin-left: 33%;
  width: 66%;
}
.About__imgs img:nth-child(2) {
  margin-top: -20%;
  width: 52%;
}
.About__imgs img:nth-child(3) {
  margin-top: -20%;
  margin-left: 40%;
  width: 40%;
}
@screen lg {
  .About__imgs img:nth-child(1) {
    margin-left: 180px;
    width: initial;
  }
  .About__imgs img:nth-child(2) {
    margin-top: -94px;
    width: initial;
  }
  .About__imgs img:nth-child(3) {
    margin-top: -142px;
    margin-left: 200px;
    width: initial;
  }
}


/** 
  Features
 */
.About__features {
  max-width: 100%;
}

@screen lg {
  .About__features {
    max-width: 405px;
  }
}

.About__features .feature {
  @apply flex items-start border-b border-blue-text border-opacity-25 mb-12 pb-12;
}

.About__features .feature:last-child {
  @apply border-none;
}

.feature .feature__content {
  @apply ml-8 border-black;
}

@screen lg {
  .feature .feature__content {
    @apply ml-12;
  }
}

.feature .feature__content h3 {
  @apply font-bold text-xl text-blue-dark mb-6 leading-none;
}

.feature .feature__content p {
  @apply text-lg text-blue-text leading-relaxed;
}
</style>