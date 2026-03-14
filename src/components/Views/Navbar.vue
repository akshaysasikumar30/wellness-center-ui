<template>
  <nav class="navbar fixed-top navbar-expand-md" style="background-color: #f7f5f0;">
    <div class="container-fluid">
      <!-- Logo + Name -->
      <a class="navbar-brand d-flex align-items-center gap-2" href="#">
        <!-- Using a leaf emoji as a placeholder; replace with SVG if you want -->
        <span style="font-size: 1.5rem; color: #5a7a4d;">🍃</span>
        <span class="sue-ellen-francisco-regular" style="color: #3d5a3c; letter-spacing: 1px; font-size: xx-large;">The Zen Nest</span>
      </a>

      <!-- Toggler for mobile -->
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <!-- Navbar links -->
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto align-items-center gap-3">
          <li class="nav-item">
            <button class="btn btn-link nav-link" @click="scrollToSection('rooms')">Rooms</button>
          </li>
          <li class="nav-item">
            <button class="btn btn-link nav-link" @click="scrollToSection('events')">Events</button>
          </li>
          <li class="nav-item">
            <button class="btn btn-link nav-link" @click="scrollToSection('restaurant')">Dining</button>
          </li>
          <li class="nav-item">
            <button class="btn btn-link nav-link" @click="scrollToSection('spa')">Spa</button>
          </li>
          <li class="nav-item">
            <button class="btn btn-link nav-link" @click="scrollToSection('wellness')">Wellness</button>
          </li>
          <li class="nav-item">
            <button class="btn btn-link nav-link" @click="scrollToSection('activities')">Activities</button>
          </li>
          <li class="nav-item">
            <button class="btn" style="background-color: #5a7a4d; color: white;" @mouseover="hover = true" @mouseleave="hover = false"
              :style="{ backgroundColor: hover ? '#4a6a3d' : '#5a7a4d' }"
            >
              Book Now
            </button>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue';

const hover = ref(false);

const scrollToSection = (id) => {
  const element = document.getElementById(id);
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' });
  }
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Sue+Ellen+Francisco&display=swap');

.sue-ellen-francisco-regular {
  font-family: "Sue Ellen Francisco", cursive;
  font-weight: 400;
  font-style: normal;
}



.navbar-nav .nav-link {
  color: #5a6b56;
  transition: color 0.3s;
}

.navbar-nav .nav-link:hover {
  color: #3d5a3c;
}
</style>
