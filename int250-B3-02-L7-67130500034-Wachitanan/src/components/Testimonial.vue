<script setup>
import profile1 from '../images-fylo/profile-1.jpg'
import profile2 from '../images-fylo/profile-2.jpg'
import profile3 from '../images-fylo/profile-3.jpg'

defineProps({
  isDark: Boolean,
})

const testimonials = [
  {
    quote:
      'Fylo has improved our team productivity by an order of magnitude. Since making the switch our team has become a well-oiled collaboration machine.',
    name: 'Satish Patel',
    title: 'Founder & CEO, Huddle',
    avatar: profile1,
  },
  {
    quote:
      'Fylo has improved our team productivity by an order of magnitude. Since making the switch our team has become a well-oiled collaboration machine.',
    name: 'Bruce McKenzie',
    title: 'Founder & CEO, Huddle',
    avatar: profile2,
  },
  {
    quote:
      'Fylo has improved our team productivity by an order of magnitude. Since making the switch our team has become a well-oiled collaboration machine.',
    name: 'Iva Boyd',
    title: 'Founder & CEO, Huddle',
    avatar: profile3,
  },
]
</script>

<template>
  <section
    id="testimonials"
    class="py-16 md:py-24 px-6 transition-colors duration-500"
    :class="isDark ? 'bg-dark-main' : 'bg-white'"
  >
    <div class="max-w-5xl mx-auto relative">
      <!-- Quote background decoration -->
      <img
        src="../images-fylo/bg-quotes.png"
        alt=""
        aria-hidden="true"
        class="absolute -top-6 left-0 w-8 md:w-12 z-0"
      />

      <!-- Testimonial cards grid -->
      <div class="relative z-10 grid grid-cols-1 md:grid-cols-3 gap-6">
        <div
          v-for="testimonial in testimonials"
          :key="testimonial.name"
          class="testimonial-card"
          :class="isDark ? 'bg-dark-testimonial text-white' : 'bg-light-section text-gray-700'"
        >
          <p class="text-sm leading-relaxed mb-6">
            {{ testimonial.quote }}
          </p>
          <div class="flex items-center gap-3">
            <img
              :src="testimonial.avatar"
              :alt="`Photo of ${testimonial.name}`"
              class="w-9 h-9 rounded-full object-cover"
            />
            <div>
              <p class="text-sm font-bold font-raleway">{{ testimonial.name }}</p>
              <p class="text-xs" :class="isDark ? 'text-gray-400' : 'text-gray-500'">
                {{ testimonial.title }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped></style>