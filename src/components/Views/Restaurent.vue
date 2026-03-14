<template>
  <!-- Using bg-white natively via inline styles to ensure no overriding -->
  <section id="restaurant" class="py-5 bg-white">
    <div class="container py-4">
      
      <!-- Heading Section -->
      <div class="text-center mb-5 pb-3">
        <p class="mb-2 text-uppercase fw-medium" style="color: #5a7a4d; letter-spacing: 1px; font-size: 0.9rem;">
          Dining
        </p>
        <h2 class="display-5 fw-semibold mb-3" style="color: #3d5a3c;">
          Taste Nature's Goodness
        </h2>
        <p class="mb-0 mx-auto" style="color: #6c757d; font-size: 1.1rem; max-width: 650px;">
          Every meal is a celebration of local flavors and mindful eating
        </p>
      </div>

      <!-- Content Grid -->
      <div class="row g-5 align-items-center mb-5 pb-4">
        
        <!-- Left Image -->
        <div class="col-12 col-lg-6">
          <div class="position-relative shadow-lg image-container">
            <img
              src="https://images.unsplash.com/photo-1651978595428-b79169f223a5?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w3Nzg4Nzd8MHwxfHNlYXJjaHwxfHxoZWFsdGh5JTIwcmVzdGF1cmFudCUyMGZvb2R8ZW58MXx8fHwxNzY2MjkyMjU1fDA&ixlib=rb-4.1.0&q=80&w=1080"
              alt="Healthy restaurant food"
              class="w-100 h-100"
              style="object-fit: cover;"
            />
          </div>
        </div>

        <!-- Right Philosophy List -->
        <div class="col-12 col-lg-6">
          <div class="d-flex flex-column gap-5">
            <div
              v-for="(item, index) in philosophy"
              :key="index"
              class="d-flex gap-4 align-items-center"
            >
              <div class="flex-shrink-0 rounded-circle d-flex align-items-center justify-content-center" style="width: 56px; height: 56px; background-color: rgba(90, 122, 77, 0.1);">
                <component
                  :is="item.icon"
                  :size="28"
                  style="color: #5a7a4d;"
                />
              </div>
              
              <div>
                <h4 class="fw-semibold mb-1" style="color: #3d5a3c;">
                  {{ item.title }}
                </h4>
                <p class="mb-0" style="color: #6c757d; font-size: 1.05rem;">
                  {{ item.description }}
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Dining Hours Card -->
      <div class="rounded-4 p-5 text-center shadow-sm" style="background-color: #f7f5f0;">
        <h3 class="fw-semibold mb-4 pb-2" style="color: #3d5a3c;">Dining Hours</h3>
        
        <div class="row g-4 justify-content-center mb-5">
          <div class="col-12 col-md-4">
            <p class="mb-1 fw-bold text-uppercase" style="color: #5a7a4d; font-size: 0.9rem; letter-spacing: 0.5px;">Breakfast</p>
            <p class="mb-0 fw-medium" style="color: #6c757d;">7:00 AM - 10:30 AM</p>
          </div>
          <div class="col-12 col-md-4">
            <p class="mb-1 fw-bold text-uppercase" style="color: #5a7a4d; font-size: 0.9rem; letter-spacing: 0.5px;">Lunch</p>
            <p class="mb-0 fw-medium" style="color: #6c757d;">12:00 PM - 3:00 PM</p>
          </div>
          <div class="col-12 col-md-4">
            <p class="mb-1 fw-bold text-uppercase" style="color: #5a7a4d; font-size: 0.9rem; letter-spacing: 0.5px;">Dinner</p>
            <p class="mb-0 fw-medium" style="color: #6c757d;">6:00 PM - 10:00 PM</p>
          </div>
        </div>
        
        <button class="btn btn-reserve px-5 py-3 fw-medium" style="font-size: 1.05rem;">
          Reserve a Table
        </button>
      </div>

    </div>
  </section>
</template>

<script setup>
import { Leaf, Sun, Droplets } from 'lucide-vue-next';

const philosophy = [
  {
    icon: Leaf,
    title: 'Farm to Table',
    description: 'Fresh ingredients from our organic gardens'
  },
  {
    icon: Sun,
    title: 'Seasonal Menu',
    description: "Nature's bounty at its peak"
  },
  {
    icon: Droplets,
    title: 'Mindful Cuisine',
    description: 'Nourish your body and soul'
  }
];
</script>

<style scoped>
.btn-reserve {
  background-color: #5a7a4d;
  color: white;
  transition: all 0.3s ease;
  border: none;
}

.btn-reserve:hover {
  background-color: #4a6a3d;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(90, 122, 77, 0.2);
  color: white;
}

.image-container {
  height: 400px;
  border-radius: 12px;
  overflow: hidden;
  transition: transform 0.3s ease;
}

.image-container:hover {
  transform: scale(1.02);
}
</style>
