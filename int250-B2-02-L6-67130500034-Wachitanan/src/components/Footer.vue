<script>
export default {
  name: 'Footer',
  data() {
    return {
      footerLinks: ['About', 'Careers', 'Events', 'Products', 'Support'],
      socials: [
        { name: 'Facebook', icon: '/src/assets/icon-facebook.svg' },
        { name: 'Twitter', icon: '/src/assets/icon-twitter.svg' },
        { name: 'Pinterest', icon: '/src/assets/icon-pinterest.svg' },
        { name: 'Instagram', icon: '/src/assets/icon-instagram.svg' },
      ],
    }
  },
}
</script>

<template>
  <footer class="bg-black text-white py-10">
    <div class="max-w-6xl mx-auto px-6 md:px-0">
      <div class="flex flex-col items-center gap-6 md:flex-row md:justify-between md:items-start">
 
        <div class="flex flex-col items-center md:items-start gap-4">
          <img src="../assets/logo.svg" alt="loopstudios" class="h-7" />

          <nav class="flex flex-col items-center gap-3 md:flex-row md:gap-6">
            <div v-for="item in footerLinks" :key="item" class="group">
              <a href="#" class="text-sm font-light text-gray-300 hover:text-white transition-colors">{{ item }}</a>
              <div class="h-[1px] w-0 group-hover:w-full bg-white transition-all duration-300 mt-0.5 mx-auto"></div>
            </div>
          </nav>
        </div>
 
        <div class="flex flex-col items-center gap-4 md:items-end">
          <div class="flex gap-4">
            <a v-for="social in socials" :key="social.name" href="#" :aria-label="social.name" class="group">
              <img :src="social.icon" :alt="social.name" class="w-5 h-5 opacity-80 group-hover:opacity-100 transition-opacity" />
              <div class="h-[1px] w-0 group-hover:w-full bg-white transition-all duration-300 mt-0.5 mx-auto"></div>
            </a>
          </div>

          <p class="text-sm text-gray-500">
            &copy; 2022 Loopstudios. All Rights Reserved.
          </p>
        </div>
 
      </div>
    </div>
  </footer>

</template>

<style>
</style>