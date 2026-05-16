<script setup>
import logoDark from '../images-fylo/logo-dark-mode.svg'
import logoLight from '../images-fylo/logo-light-mode.svg'

defineProps({
  isDark: Boolean,
})

const emit = defineEmits(['toggle-dark'])
</script>

<template>
  <nav
    class="w-full px-6 md:px-12 lg:px-20 py-8 flex items-center justify-between transition-colors duration-500"
    :class="isDark ? 'bg-dark-intro' : 'bg-white'"
  >
    <!-- logo fylo -->
    <a href="#" aria-label="Fylo home">
      <img
        :src="isDark ? logoDark : logoLight"
        alt="Fylo logo"
        class="w-24 md:w-32 lg:w-40"
      />
    </a>

    <!-- Nav links + dark mode toggle -->
    <div class="flex items-center gap-6 md:gap-10">
      <a href="#features" class="nav-link" :class="isDark ? 'text-white' : 'text-gray-700'">Features</a>
      <a href="#faq" class="nav-link" :class="isDark ? 'text-white' : 'text-gray-700'">FAQs</a>
      <a href="#testimonials" class="nav-link" :class="isDark ? 'text-white' : 'text-gray-700'">Testimonials</a>

      <!-- Dark mode toggle-->
      <button
        @click="emit('toggle-dark')"
        :aria-label="isDark ? 'Switch to light mode' : 'Switch to dark mode'"
        class="w-7 h-7 flex items-center justify-center transition-transform duration-300 hover:scale-110 focus:outline-none hover:bg-slate-200 hover:rounded-xl"
      >
        <!-- Moon icon in light mode -->
        <svg
          v-if="!isDark"
          xmlns="http://www.w3.org/2000/svg"
          class="w-6 h-6 text-gray-600"
          fill="currentColor"
          viewBox="0 0 24 24"
          aria-hidden="true"
        >
          <path d="M21.752 15.002A9.718 9.718 0 0 1 18 15.75 9.75 9.75 0 0 1 8.25 6a9.718 9.718 0 0 1 .248-2.252A9.75 9.75 0 0 0 12 21.75c3.913 0 7.297-2.31 8.998-5.67a.75.75 0 0 0-.998-1.002l-.248.924z"/>
        </svg>

        
        <svg
          v-else
          xmlns="http://www.w3.org/2000/svg"
          class="w-6 h-6 text-yellow-300"
          fill="currentColor"
          viewBox="0 0 24 24"
          aria-hidden="true"
        >
          <path d="M12 2.25a.75.75 0 0 1 .75.75v2.25a.75.75 0 0 1-1.5 0V3a.75.75 0 0 1 .75-.75zM12 18.75a.75.75 0 0 1 .75.75V21a.75.75 0 0 1-1.5 0v-1.5a.75.75 0 0 1 .75-.75zM2.25 12a.75.75 0 0 1 .75-.75H4.5a.75.75 0 0 1 0 1.5H3a.75.75 0 0 1-.75-.75zM19.5 12a.75.75 0 0 1 .75-.75H21a.75.75 0 0 1 0 1.5h-1.5a.75.75 0 0 1-.75-.75zM5.636 5.636a.75.75 0 0 1 1.06 0l1.06 1.061a.75.75 0 0 1-1.06 1.06l-1.06-1.06a.75.75 0 0 1 0-1.061zM16.243 16.243a.75.75 0 0 1 1.061 0l1.06 1.061a.75.75 0 0 1-1.06 1.06l-1.061-1.06a.75.75 0 0 1 0-1.061zM5.636 18.364a.75.75 0 0 1 0-1.06l1.061-1.061a.75.75 0 1 1 1.06 1.06l-1.06 1.061a.75.75 0 0 1-1.061 0zM16.243 7.757a.75.75 0 0 1 0-1.06l1.061-1.061a.75.75 0 1 1 1.06 1.06l-1.06 1.061a.75.75 0 0 1-1.061 0zM12 6.75a5.25 5.25 0 1 0 0 10.5 5.25 5.25 0 0 0 0-10.5z"/>
        </svg>
      </button>
    </div>
  </nav>
</template>
