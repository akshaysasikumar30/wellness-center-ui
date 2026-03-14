<template>
  <section id="events" class="py-5" style="background-color: #f7f5f0;">
    <div class="container py-4">
      <div class="row g-5 align-items-center">

        <!-- Left Content -->
        <div class="col-12 col-lg-6">
          <p class="mb-2 text-uppercase fw-medium" style="color: #5a7a4d; letter-spacing: 1px; font-size: 0.9rem;">
            Event Spaces
          </p>

          <h2 class="display-5 fw-semibold mb-4" style="color: #3d5a3c;">
            Celebrate Life's Moments in Nature
          </h2>

          <p class="mb-5" style="color: #6c757d; font-size: 1.1rem; line-height: 1.6;">
            Our versatile event spaces blend seamlessly with the natural landscape,
            providing the perfect backdrop for weddings, retreats, and corporate gatherings.
          </p>

          <div class="d-flex flex-column gap-4 mb-5">

            <div
              v-for="(event, index) in events"
              :key="index"
              class="d-flex gap-3"
            >
              <div class="flex-shrink-0 rounded-circle d-flex align-items-center justify-content-center" style="width: 48px; height: 48px; background-color: rgba(90, 122, 77, 0.1);">
                <component
                  :is="event.icon"
                  :size="24"
                  style="color: #5a7a4d;"
                />
              </div>

              <div>
                <h5 class="fw-semibold mb-1" style="color: #3d5a3c;">
                  {{ event.title }}
                </h5>

                <p class="mb-1" style="color: #6c757d; font-size: 0.95rem;">
                  {{ event.description }}
                </p>

                <p class="mb-0 fw-medium" style="color: #B8965A; font-size: 0.85rem;">
                  {{ event.capacity }}
                </p>
              </div>
            </div>

          </div>

          <button class="btn btn-event px-4 py-2 fw-medium">
            Plan Your Event
          </button>

        </div>

        <!-- Right Image -->
        <div class="col-12 col-lg-6">
          <div class="position-relative shadow-lg image-container">
            <img
              src="/assets/ariel-domenden-3Ki7QC0jVEg-unsplash.jpg"
              alt="Beautiful garden event venue"
              class="w-100 h-100"
              style="object-fit: cover;"
            />
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
import { Calendar, Heart, Briefcase } from "lucide-vue-next";

const events = [
  {
    title: "Outdoor Ceremonies",
    description: "Create magical moments under open skies",
    icon: Heart,
    capacity: "Up to 150 guests",
  },
  {
    title: "Wellness Retreats",
    description: "Host transformative group experiences",
    icon: Calendar,
    capacity: "Up to 80 guests",
  },
  {
    title: "Corporate Events",
    description: "Inspire your team in nature",
    icon: Briefcase,
    capacity: "Up to 100 guests",
  },
];
</script>

<style scoped>
.btn-event {
  background-color: #3d5a3c;
  color: white;
  transition: all 0.3s ease;
}

.btn-event:hover {
  background-color: #4a6a3d;
  color: white;
  transform: translateY(-2px);
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
}

.image-container {
  height: 500px;
  border-radius: 12px;
  overflow: hidden;
  transition: transform 0.3s ease;
}

.image-container:hover {
  transform: scale(1.02);
}
</style>
