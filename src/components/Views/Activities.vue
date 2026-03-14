<template>
  <section id="activities" class="py-5" style="background-color: #f7f5f0;">
    <div class="container py-4">
      
      <!-- Heading Section -->
      <div class="text-center mb-5 pb-3">
        <p class="mb-2 text-uppercase fw-medium" style="color: #8ba882; letter-spacing: 1px; font-size: 0.9rem;">
          Activities
        </p>
        <h2 class="display-5 fw-semibold mb-3" style="color: #3d5a3c;">
          Connect with Nature
        </h2>
        <p class="mb-0 mx-auto" style="color: #6c757d; font-size: 1.1rem; max-width: 650px;">
          Immerse yourself in outdoor experiences that awaken your senses and renew your spirit
        </p>
      </div>

      <!-- Activities Grid -->
      <div class="row g-4 mb-4">
        <div 
          v-for="(activity, index) in activities" 
          :key="index"
          class="col-12 col-md-6 col-lg-4"
        >
          <div 
            class="card activity-card h-100 p-4 border-0 text-center"
            style="border: 1px solid #d4c5a3 !important; border-radius: 12px; transition: all 0.3s ease;"
          >
            <div class="d-flex flex-column align-items-center h-100">
              <div 
                class="rounded-circle d-flex align-items-center justify-content-center mb-4" 
                style="width: 64px; height: 64px; background-color: rgba(139, 168, 130, 0.2);"
              >
                <component
                  :is="activity.icon"
                  :size="32"
                  style="color: #5a7a4d;"
                />
              </div>
              
              <h4 class="fw-semibold mb-3" style="color: #3d5a3c;">{{ activity.name }}</h4>
              <p class="mb-4" style="color: #6c757d; font-size: 0.95rem;">{{ activity.description }}</p>
              
              <!-- Time Badge -->
              <span 
                class="mt-auto rounded-pill fw-medium" 
                style="color: #8ba882; background-color: rgba(139, 168, 130, 0.1); font-size: 0.85rem; padding: 0.4em 1em;"
              >
                {{ activity.time }}
              </span>
            </div>
          </div>
        </div>
      </div>

      <!-- Footer Info -->
      <div class="text-center mt-5 pt-3">
        <p class="mb-2" style="color: #6c757d; font-size: 1.05rem;">
          All activities are complimentary for resort guests
        </p>
        <p class="mb-0 fw-medium" style="color: #8ba882; font-size: 0.9rem;">
          Advanced booking recommended for guided experiences
        </p>
      </div>

    </div>
  </section>
</template>

<script setup>
import { Bird, Mountain, Bike, Waves, TreePine, Camera } from 'lucide-vue-next';

const activities = [
  {
    icon: Bird,
    name: 'Bird Watching',
    description: 'Observe native species in their natural habitat',
    time: 'Early morning'
  },
  {
    icon: Mountain,
    name: 'Nature Hikes',
    description: 'Explore scenic trails through forests and meadows',
    time: 'All day'
  },
  {
    icon: Bike,
    name: 'Cycling Tours',
    description: 'Discover the countryside on two wheels',
    time: 'Morning & evening'
  },
  {
    icon: Waves,
    name: 'Water Activities',
    description: 'Kayaking and peaceful lake experiences',
    time: 'Afternoon'
  },
  {
    icon: TreePine,
    name: 'Forest Bathing',
    description: 'Japanese Shinrin-yoku guided sessions',
    time: 'Afternoon'
  },
  {
    icon: Camera,
    name: 'Photography Walks',
    description: 'Capture the beauty of nature with expert guides',
    time: 'Golden hour'
  }
];
</script>

<style scoped>
.activity-card {
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05), 0 2px 4px -1px rgba(0, 0, 0, 0.03);
}

.activity-card:hover {
  box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04) !important;
  transform: translateY(-4px);
}
</style>
