<script setup>
defineProps({
  isDark: Boolean,
})

const aboutLinks = ['About', 'Jobs', 'Press', 'Blog']
const contactLinks = ['Contact Us', 'Terms', 'Privacy']
</script>

<template>
  <footer
    class="py-12 md:py-16 px-6 md:px-12 lg:px-20 transition-colors duration-500"
    :class="isDark ? 'bg-dark-footer text-white' : 'bg-gray-800 text-white'"
  >
    <div class="max-w-6xl mx-auto">
      
      <img
        src="../images-fylo/logo-light-mode.svg"
        alt="Fylo"
        class="w-32 md:w-40 mb-8"
      />

      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-8 md:gap-12 lg:gap-16">
        <div class="sm:col-span-2 md:col-span-1">
          <div class="flex items-start gap-4 mb-4">
            <img
              src="../images-fylo/icon-location.svg"
              alt=""
              aria-hidden="true"
              class="w-5 h-5 mt-1 flex-shrink-0"
            />
            <p class="text-sm leading-relaxed text-gray-300">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
              eiusmod tempor incididunt.
            </p>
          </div>
          <div class="flex items-center gap-4 mb-3">
            <img
              src="../images-fylo/icon-phone.svg"
              alt="Phone"
              class="w-5 h-5 flex-shrink-0"
            />
            <a href="tel:+15431224607" class="text-sm text-gray-300 hover:text-cyan-fylo transition-colors">
              +1-543-123-4567
            </a>
          </div>
          <div class="flex items-center gap-4">
            <img
              src="../images-fylo/icon-email.svg"
              alt="Email"
              class="w-5 h-5 flex-shrink-0"
            />
            <a href="mailto:example@fylo.com" class="text-sm text-gray-300 hover:text-cyan-fylo transition-colors">
              example@fylo.com
            </a>
          </div>
        </div>

        <!-- About links -->
        <nav aria-label="About links">
          <ul class="space-y-3">
            <li v-for="link in aboutLinks" :key="link">
              <a href="#" class="text-sm text-gray-300 hover:text-cyan-fylo transition-colors">
                {{ link }}
              </a>
            </li>
          </ul>
        </nav>

        <!-- Contact links -->
        <nav aria-label="Contact links">
          <ul class="space-y-3">
            <li v-for="link in contactLinks" :key="link">
              <a href="#" class="text-sm text-gray-300 hover:text-cyan-fylo transition-colors">
                {{ link }}
              </a>
            </li>
          </ul>
        </nav>

        <!-- Social icons -->
        <div class="flex items-start gap-4">
          <a
            href="https://facebook.com"
            target="_blank"
            rel="noopener noreferrer"
            aria-label="Facebook"
            class="w-9 h-9 rounded-full border border-gray-400 flex items-center justify-center hover:border-cyan-fylo hover:text-cyan-fylo transition-colors"
          >
            <img src="../images-fylo/facebook.svg" alt="Facebook" class="w-4 h-4" />
          </a>
          <a
            href="https://twitter.com"
            target="_blank"
            rel="noopener noreferrer"
            aria-label="Twitter"
            class="w-9 h-9 rounded-full border border-gray-400 flex items-center justify-center hover:border-cyan-fylo hover:text-cyan-fylo transition-colors"
          >
            <img src="../images-fylo/twitter.svg" alt="Twitter" class="w-4 h-4" />
          </a>
          <a
            href="https://instagram.com"
            target="_blank"
            rel="noopener noreferrer"
            aria-label="Instagram"
            class="w-9 h-9 rounded-full border border-gray-400 flex items-center justify-center hover:border-cyan-fylo hover:text-cyan-fylo transition-colors"
          >
            <img src="../images-fylo/instagram.svg" alt="Instagram" class="w-4 h-4" />
          </a>
        </div>
      </div>
    </div>
  </footer>
</template>

<style scoped></style>