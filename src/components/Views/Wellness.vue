<template>
  <section id="wellness" class="py-5 bg-white">
    <div class="container py-4">
      
      <!-- Heading Section -->
      <div class="text-center mb-5 pb-3">
        <p class="mb-2 text-uppercase fw-medium" style="color: #5a7a4d; letter-spacing: 1px; font-size: 0.9rem;">
          Wellness & Fitness
        </p>
        <h2 class="display-5 fw-semibold mb-3" style="color: #3d5a3c;">
          Your Journey to Wholeness
        </h2>
        <p class="mb-0 mx-auto" style="color: #6c757d; font-size: 1.1rem; max-width: 650px;">
          We offer comprehensive wellness programs to nurture your mind, body, and spirit
        </p>
      </div>

      <!-- Facilities Grid -->
      <div class="row g-4 mb-5">
        <div 
          v-for="(facility, index) in facilities" 
          :key="index"
          class="col-12 col-md-6"
        >
          <div 
            class="card facility-card h-100 p-4 border-0 shadow-sm"
            style="border: 1px solid #e8e0d0 !important; border-radius: 12px; transition: all 0.3s ease;"
          >
            <!-- Header -->
            <div class="d-flex align-items-start gap-4 mb-4">
              <div class="flex-shrink-0 rounded-circle d-flex align-items-center justify-content-center" style="width: 56px; height: 56px; background-color: rgba(90, 122, 77, 0.1);">
                <component
                  :is="facility.icon"
                  :size="28"
                  style="color: #5a7a4d;"
                />
              </div>
              <div>
                <h4 class="fw-semibold mb-2" style="color: #3d5a3c;">{{ facility.title }}</h4>
                <p class="mb-0" style="color: #6c757d; font-size: 1.05rem;">{{ facility.description }}</p>
              </div>
            </div>
            
            <!-- Features List -->
            <ul class="list-unstyled mb-0 d-flex flex-column gap-2 mt-auto">
              <li 
                v-for="(feature, idx) in facility.features" 
                :key="idx" 
                class="d-flex align-items-center gap-2"
                style="color: #6c757d; font-size: 0.95rem;"
              >
                <div class="rounded-circle" style="width: 6px; height: 6px; background-color: #5a7a4d;"></div>
                {{ feature }}
              </li>
            </ul>
          </div>
        </div>
      </div>

      <!-- Consultation CTA -->
      <div 
        class="rounded-4 p-5 text-center mt-5" 
        style="background: linear-gradient(to right, rgba(139, 168, 130, 0.2), rgba(212, 197, 163, 0.2)); border-radius: 12px; border: 1px solid rgba(139, 168, 130, 0.1);"
      >
        <h3 class="fw-semibold mb-3" style="color: #3d5a3c;">
          Ready to Transform Your Wellness?
        </h3>
        <p class="mb-4 mx-auto" style="color: #6c757d; font-size: 1.05rem; max-width: 650px;">
          Our wellness team is here to create a personalized program just for you
        </p>
        <button class="btn btn-consult px-4 py-2 fw-medium" style="font-size: 1.05rem;">
          Schedule Consultation
        </button>
      </div>

    </div>
  </section>
</template>

<script setup>
import { Dumbbell, Heart, Brain, Sunrise } from 'lucide-vue-next';

const facilities = [
  {
    icon: Dumbbell,
    title: 'Fitness Center',
    description: 'State-of-the-art equipment with forest views',
    features: ['Cardio machines', 'Free weights', 'Yoga mats', 'Personal training']
  },
  {
    icon: Brain,
    title: 'Meditation Garden',
    description: 'Find inner peace in our tranquil garden',
    features: ['Guided sessions', 'Private spaces', 'Sound healing', 'Mindfulness classes']
  },
  {
    icon: Sunrise,
    title: 'Morning Rituals',
    description: 'Start your day with intention',
    features: ['Sunrise yoga', 'Breathing exercises', 'Nature walks', 'Tea ceremonies']
  },
  {
    icon: Heart,
    title: 'Wellness Programs',
    description: 'Customized journeys to better health',
    features: ['Nutrition counseling', 'Fitness plans', 'Stress management', 'Life coaching']
  }
];
</script>

<style scoped>
.facility-card:hover {
  box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04) !important;
  transform: translateY(-4px);
}

.btn-consult {
  background-color: #5a7a4d;
  color: white;
  transition: all 0.3s ease;
  border: none;
  border-radius: 8px;
}

.btn-consult:hover {
  background-color: #4a6a3d;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(90, 122, 77, 0.2);
  color: white;
}
</style>
