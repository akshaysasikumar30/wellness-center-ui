<template>
  <!-- Using #e8e0d0 at 30% opacity to match the provided bg-[#e8e0d0]/30 -->
  <section id="spa" class="py-5" style="background-color: rgba(232, 224, 208, 0.3);">
    <div class="container py-4">
      
      <!-- Heading Section -->
      <div class="text-center mb-5 pb-3">
        <p class="mb-2 text-uppercase fw-medium" style="color: #5a7a4d; letter-spacing: 1px; font-size: 0.9rem;">
          Spa & Beauty
        </p>
        <h2 class="display-5 fw-semibold mb-3" style="color: #3d5a3c;">
          Nurture Your Body & Spirit
        </h2>
        <p class="mb-0 mx-auto" style="color: #6c757d; font-size: 1.1rem; max-width: 650px;">
          Surrender to tranquility with our holistic treatments inspired by nature
        </p>
      </div>

      <!-- Content Grid -->
      <div class="row g-5 mb-4">
        
        <!-- Left Image -->
        <div class="col-12 col-lg-6">
          <div class="position-relative shadow-lg image-container h-100 min-vh-50">
            <img
              src="https://images.unsplash.com/photo-1757689314932-bec6e9c39e51?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w3Nzg4Nzd8MHwxfHNlYXJjaHwxfHxzcGElMjB3ZWxsbmVzcyUyMG1hc3NhZ2V8ZW58MXx8fHwxNzY2MjE5MDE2fDA&ixlib=rb-4.1.0&q=80&w=1080"
              alt="Spa wellness massage"
              class="w-100 h-100 position-absolute top-0 start-0"
              style="object-fit: cover;"
            />
          </div>
        </div>

        <!-- Right Content Area -->
        <div class="col-12 col-lg-6 d-flex flex-column">
          
          <h3 class="fw-semibold mb-4" style="color: #3d5a3c;">Spa Treatments</h3>
          
          <!-- Treatments List -->
          <div class="d-flex flex-column gap-3 mb-5">
            <div
              v-for="(treatment, index) in treatments"
              :key="index"
              class="card treatment-card p-3 border-0 shadow-sm"
              style="border: 1px solid #d4c5a3 !important; border-radius: 12px; transition: all 0.3s ease;"
            >
              <div class="d-flex gap-3">
                <div class="flex-shrink-0 rounded-circle d-flex align-items-center justify-content-center" style="width: 48px; height: 48px; background-color: rgba(90, 122, 77, 0.1);">
                  <component
                    :is="treatment.icon"
                    :size="24"
                    style="color: #5a7a4d;"
                  />
                </div>
                
                <div class="flex-grow-1">
                  <div class="d-flex justify-content-between align-items-start mb-1">
                    <h5 class="fw-semibold mb-0" style="color: #3d5a3c;">{{ treatment.name }}</h5>
                    <span class="fw-medium" style="color: #5a7a4d; font-size: 0.9rem;">{{ treatment.duration }}</span>
                  </div>
                  <p class="mb-0" style="color: #6c757d; font-size: 0.95rem;">{{ treatment.description }}</p>
                </div>
              </div>
            </div>
          </div>

          <!-- Beauty Services -->
          <h3 class="fw-semibold mb-4" style="color: #3d5a3c;">Beauty Services</h3>
          <div class="row g-3 mb-5">
            <div 
              v-for="(service, index) in beautyServices" 
              :key="index" 
              class="col-6 d-flex align-items-center gap-2"
            >
              <div class="rounded-circle" style="width: 8px; height: 8px; background-color: #5a7a4d;"></div>
              <span style="color: #6c757d; font-size: 0.95rem;">{{ service }}</span>
            </div>
          </div>

          <!-- Book Button -->
          <button class="btn btn-book w-100 py-3 mt-auto fw-medium" style="font-size: 1.05rem;">
            Book Treatment
          </button>

        </div>
      </div>

    </div>
  </section>
</template>

<script setup>
import { Sparkles, Flower2, Hand } from 'lucide-vue-next';

const treatments = [
  {
    name: 'Signature Massage',
    duration: '60-90 min',
    description: 'Deep relaxation with organic essential oils',
    icon: Hand
  },
  {
    name: 'Herbal Facial',
    duration: '60 min',
    description: 'Rejuvenate with plant-based treatments',
    icon: Flower2
  },
  {
    name: 'Body Treatments',
    duration: '90 min',
    description: 'Full body wellness experience',
    icon: Sparkles
  }
];

const beautyServices = [
  'Manicure & Pedicure',
  'Hair Styling',
  'Natural Hair Treatments',
  'Scalp Massage'
];
</script>

<style scoped>
.treatment-card:hover {
  box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05) !important;
  transform: translateY(-2px);
}

.btn-book {
  background-color: #5a7a4d;
  color: white;
  transition: all 0.3s ease;
  border: none;
  border-radius: 8px;
}

.btn-book:hover {
  background-color: #4a6a3d;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(90, 122, 77, 0.2);
  color: white;
}

.image-container {
  min-height: 500px;
  border-radius: 12px;
  overflow: hidden;
  transition: transform 0.3s ease;
}

.image-container:hover {
  transform: scale(1.02);
}

@media (max-width: 991.98px) {
  .image-container {
    min-height: 400px;
  }
}
</style>
