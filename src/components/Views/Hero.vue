<template>
  <div>

    <!-- Full screen image section -->
    <section class="vh-100 position-relative">

      <!-- Background Image -->
      <img 
        src="/assets/sasha-kaunas-xEaAoizNFV8-unsplash.jpg"
        class="w-100 h-100 object-fit-cover"
        alt="hero image"
      >

      <!-- Centered Content -->
      <div class="position-absolute top-50 start-50 translate-middle text-center text-white px-3 w-100">

        <!-- Responsive Heading -->
        <h1 class="fw-semibold mb-3 display-6 display-md-4 display-lg-3" 
            :style="{ color: '#3d5a3c' }">
          Welcome to The Zen Nest
        </h1>

        <!-- Responsive Subtitle -->
        <h5 class="mb-3 mt-2 px-2" :style="{ color: '#B8965A' }">
          Reconnect with nature's gentle whispers
        </h5>

        <!-- Responsive Paragraph -->
        <p class="mb-4 mx-auto px-2"
           style="max-width: 650px; font-size: 1rem;">
          Feel the breeze touch your skin. Bask in morning sunlight.
          Breathe in the earthy scent of rain. Rediscover the small,
          beautiful moments your daily life has made you miss.
        </p>

        <!-- Responsive Buttons -->
        <div class="d-flex flex-column flex-sm-row justify-content-center gap-3">

          <button class="btn px-4 py-2"
                  style="background-color: #3d5a3c; color: white">
            Begin Your Journey
          </button>

          <button class="btn btn-outline-light px-4 py-2">
            Explore More
          </button>

        </div>

      </div>

    </section>

  </div>
</template>