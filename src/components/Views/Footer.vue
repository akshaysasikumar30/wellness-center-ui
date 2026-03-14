<template>
  <footer class="py-5" style="background-color: #3d5a3c; color: white;">
    <div class="container py-4">
      <div class="row g-5 mb-5">
        
        <!-- Brand Section -->
        <div class="col-12 col-md-3">
          <div class="d-flex align-items-center gap-2 mb-4">
            <component :is="Leaf" :size="24" />
            <span class="fs-5 fw-semibold">The Zen Nest</span>
          </div>
          <p style="color: #c8d5c4; line-height: 1.6;">
            Your sanctuary for mental and physical wellbeing, 
            nestled in nature's embrace.
          </p>
        </div>

        <!-- Quick Links -->
        <div class="col-12 col-md-3">
          <h5 class="mb-4 fw-semibold">Quick Links</h5>
          <ul class="list-unstyled d-flex flex-column gap-2 mb-0" style="color: #c8d5c4;">
            <li><a href="#rooms" class="footer-link">Rooms</a></li>
            <li><a href="#events" class="footer-link">Events</a></li>
            <li><a href="#restaurant" class="footer-link">Dining</a></li>
            <li><a href="#spa" class="footer-link">Spa</a></li>
            <li><a href="#wellness" class="footer-link">Wellness</a></li>
            <li><a href="#activities" class="footer-link">Activities</a></li>
          </ul>
        </div>

        <!-- Contact Info -->
        <div class="col-12 col-md-3">
          <h5 class="mb-4 fw-semibold">Contact</h5>
          <ul class="list-unstyled d-flex flex-column gap-3 mb-0" style="color: #c8d5c4;">
            <li class="d-flex align-items-center gap-2">
              <component :is="Phone" :size="16" />
              <span>+1 (555) 123-4567</span>
            </li>
            <li class="d-flex align-items-center gap-2">
              <component :is="Mail" :size="16" />
              <span>hello@thezennest.com</span>
            </li>
            <li class="d-flex align-items-start gap-2">
              <component :is="MapPin" :size="16" class="mt-1" />
              <span>123 Serenity Lane<br />Peaceful Valley, Nature's Haven</span>
            </li>
          </ul>
        </div>

        <!-- Hours -->
        <div class="col-12 col-md-3">
          <h5 class="mb-4 fw-semibold">Hours</h5>
          <div class="d-flex flex-column gap-2" style="color: #c8d5c4;">
            <p class="mb-0">Check-in: 3:00 PM</p>
            <p class="mb-0">Check-out: 11:00 AM</p>
            <p class="mb-0 mt-3">Reception: 24/7</p>
          </div>
        </div>

      </div>

      <!-- Copyright Bar -->
      <div 
        class="pt-4 text-center border-top" 
        style="border-color: #5a7a4d !important; color: #c8d5c4; font-size: 0.95rem;"
      >
        <p class="mb-0">&copy; 2025 The Zen Nest. All rights reserved. Built with love for nature.</p>
      </div>
    </div>
  </footer>
</template>

<script setup>
import { Leaf, Mail, Phone, MapPin } from 'lucide-vue-next';
</script>

<style scoped>
.footer-link {
  color: #c8d5c4;
  text-decoration: none;
  transition: color 0.3s ease;
}

.footer-link:hover {
  color: white;
}
</style>
