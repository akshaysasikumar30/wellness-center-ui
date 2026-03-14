<template>
  <section id="rooms" class="min-vh-100 d-flex align-items-center py-5" style="background-color: #fcfbf8;">
    <div class="container">
      <!-- Header -->
      <div class="text-center mb-5">
        <h3 class="fw-medium mb-2" style="color: #5a7a4d; font-size: 1.5rem; letter-spacing: 1px;">
          Accomodations
        </h3>
        <h2 class="display-4 fw-semibold mb-3" style="color: #3d5a3c;">
          Your Sanctuary Awaits
        </h2>
        <p class="mb-0 mx-auto" style="color: #6c757d; font-size: 1.1rem; max-width: 650px;">
          Each room is thoughtfully designed to bring you closer to nature's embrace
        </p>
      </div>

      <!-- Room Cards -->
      <div class="row g-4 justify-content-center">
        <div 
          v-for="(room, index) in roomTypes" 
          :key="index" 
          class="col-12 col-md-6 col-lg-4"
        >
          <div class="card h-100 border-0 shadow-sm" style="border-radius: 12px; overflow: hidden; transition: transform 0.3s ease;">
            <!-- Image with responsive fit -->
            <img 
              :src="room.image" 
              class="card-img-top w-100" 
              style="height: 250px; object-fit: cover;" 
              :alt="room.name" 
            />
            
            <div class="card-body d-flex flex-column p-4">
              <div class="d-flex align-items-center mb-3">
                <component :is="room.icon" class="me-2" style="color: #5a7a4d;" :size="24" />
                <h4 class="card-title fw-semibold mb-0" style="color: #3d5a3c; font-size: 1.25rem;">{{ room.name }}</h4>
              </div>
              
              <p class="card-text mb-4" style="color: #6c757d;">
                {{ room.description }}
              </p>
              
              <div class="mb-4 flex-grow-1">
                <p class="mb-3 fw-medium" style="color: #5a7a4d; font-size: 0.85rem;">
                  Capacity: {{ room.capacity }}
                </p>

                <h6 class="fw-bold mb-2" style="color: #5a7a4d; font-size: 0.85rem; letter-spacing: 0.5px;">FEATURES</h6>
                <ul class="mb-0 ps-3" style="color: #5a7a4d; font-size: 0.9rem;">
                  <li 
                    v-for="(feature, fIndex) in room.features" 
                    :key="fIndex"
                    class="mb-1"
                  >
                    {{ feature }}
                  </li>
                </ul>
              </div>

              <div class="mt-auto pt-3 border-top">
                <button class="btn w-100 py-2 fw-medium" style="background-color: #3d5a3c; color: white;">
                  Reserve Room
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { Trees, Mountain, Users } from 'lucide-vue-next';

const roomTypes = [
  {
    name: 'Garden View Room',
    description: 'Wake up to the gentle rustle of leaves and morning birdsong',
    capacity: '2 guests',
    icon: Trees,
    image: '/assets/datingscout-JTUmzXLoqHQ-unsplash (1).jpg',
    features: ['Private balcony', 'Garden view', 'Natural light', 'Eco-friendly amenities']
  },
  {
    name: 'Forest Suite',
    description: 'Immerse yourself in nature with panoramic forest views',
    capacity: '2-3 guests',
    icon: Mountain,
    image: '/assets/forestroom.jpg',
    features: ['Spacious suite', 'Forest panorama', 'Reading nook', 'Meditation corner']
  },
  {
    name: 'Family Nest',
    description: 'Share the tranquility of nature with your loved ones',
    capacity: '4-6 guests',
    icon: Users,
    image: 'assets/hoi-an-and-da-nang-photographer-XhVclZNoEeA-unsplash.jpg',
    features: ['Two bedrooms', 'Living area', 'Terrace', 'Family activities']
  }
];
</script>

<style scoped>
.card {
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}
.card:hover {
  transform: translateY(-8px) !important;
  box-shadow: 0 1rem 3rem rgba(0,0,0,.1) !important;
}
</style>
