<script setup>
import { ref } from 'vue'
import NavBar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import Features from './components/Features.vue'
import Productive from './components/Productive.vue'
import FAQ from './components/FAQ.vue'
import Testimonial from './components/Testimonial.vue'
import EarlyAccess from './components/EarlyAccess.vue'
import Footer from './components/Footer.vue'

const isDark = ref(false)

function toggleDark() {
  isDark.value = !isDark.value
}
</script>
<template>
  <div :class="isDark ? 'dark' : ''">
    <div
      class="min-h-screen transition-colors duration-500"
      :class="isDark
        ? 'bg-dark-main text-white'
        : 'bg-white text-gray-700'"
    >
      <NavBar :isDark="isDark" @toggle-dark="toggleDark" />
      <Hero :isDark="isDark" />
      <Features :isDark="isDark" />
      <Productive :isDark="isDark" />
      <FAQ :isDark="isDark" />
      <Testimonial :isDark="isDark" />
      <EarlyAccess :isDark="isDark" />
      <Footer :isDark="isDark" />
    </div>
  </div>
</template>