<script setup>
import bgCurvyDark from '../images-fylo/bg-curvy-dark-mode.svg'
import bgCurvyLight from '../images-fylo/bg-curvy-light-mode.svg'

defineProps({
  isDark: Boolean,
})
</script>

<template>
  <section
    class="relative text-center px-6 pb-28 sm:pb-36 md:pb-48 transition-colors duration-500"
    :class="isDark ? 'bg-dark-intro' : 'bg-white'"
  >
    
    <div
      class="absolute bottom-0 left-0 w-full leading-none pointer-events-none"
    >
      <img
        :src="isDark ? bgCurvyDark : bgCurvyLight"
        alt=""
        aria-hidden="true"
        class="w-full"
      />
    </div>

    
    <div class="relative z-10 max-w-3xl mx-auto">
    
      <img
        src="../images-fylo/illustration-intro.png"
        alt="Files stored in Fylo cloud"
        class="mx-auto w-full max-w-xs sm:max-w-sm md:max-w-md lg:max-w-lg mb-8"
      />

      <h1
        class="text-2xl sm:text-3xl md:text-4xl font-bold font-raleway mb-6 leading-tight"
        :class="isDark ? 'text-white' : 'text-gray-800'"
      >
        All your files in one secure location,<br />accessible anywhere.
      </h1>

      <p
        class="text-sm md:text-base mb-8 max-w-xl mx-auto leading-relaxed"
        :class="isDark ? 'text-gray-300' : 'text-gray-600'"
      >
        Fylo stores all your most important files in one secure location.
        Access them whenever you need, share and collaborate with friends,
        family, and co-workers.
      </p>

      <a href="#early-access" class="btn-primary inline-block">
        Get Started
      </a>
    </div>
  </section>
</template>

<style scoped></style>