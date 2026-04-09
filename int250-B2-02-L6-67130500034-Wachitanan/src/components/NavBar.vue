<script>
export default {
  name: 'NavBar',
  data() {
    return {
      menuOpen: false,
      menuItems: ['About', 'Careers', 'Events', 'Products', 'Support'],
    }
  },
  computed: {
    isMobile() {
      if (typeof window !== 'undefined') {
        return window.innerWidth < 768
      }
      return false
    }
  },
  methods: {
    toggleMenu() {
      this.menuOpen = !this.menuOpen
    }
  }
}
</script>

<template>

  <section
    class="bg-cover bg-no-repeat bg-center min-h-[550px] md:min-h-[650px]"
    :style="{
      backgroundImage: isMobile
        ? 'url(/src/assets/mobile/image-hero.jpg)'
        : 'url(/src/assets/desktop/image-hero.jpg)'
    }"
  >

    <div class="@container max-w-6xl mx-auto px-6 py-12">

      <nav class="flex justify-between items-center font-bold text-white">
        
        <img src="../assets/logo.svg" alt="loopstudios" class="h-8" />

        <div class="hidden h-10 font-sans md:flex md:items-center md:space-x-8">
          <div v-for="item in menuItems" :key="item" class="group">
            <a href="#" class="text-sm font-normal tracking-wide text-white">{{ item }}</a>
            <div class="h-[2px] w-0 group-hover:w-full bg-white transition-all duration-300 mt-1 mx-auto"></div>
          </div>
        </div>

        <button
          class="md:hidden focus:outline-none"
          @click="toggleMenu"
          aria-label="Open menu"
        >
          <img src="../assets/icon-hamburger.svg" alt="menu" class="w-6 h-auto" />
        </button>
      </nav>

      <div class="mt-24 md:mt-32 max-w-lg">
        <div class="border-2 border-white mx-2 p-6 md:p-8 group hover:border-blue-50 transition-colors duration-300">
          <h1
            class="font-josefin text-4xl md:text-5xl lg:text-6xl uppercase text-white font-thin leading-tight tracking-wider"
          >
            Impressive<br />Experiences<br />That Deliver
          </h1>
        </div>
      </div>
    </div>

    <div
      v-if="menuOpen"
      class="fixed inset-0 z-50 bg-black flex flex-col px-6 py-12"
    >
      <div class="flex justify-between items-center mb-16">
        <img src="../assets/logo.svg" alt="loopstudios" class="h-8" />
        <button @click="toggleMenu" aria-label="Close menu">
          <img src="../assets/icon-close.svg" alt="close" class="w-5 h-5" />
        </button>
      </div>
      <nav class="flex flex-col space-y-6">
        <a
          v-for="item in menuItems"
          :key="item"
          href="#"
          class="text-white text-3xl uppercase font-josefin font-light tracking-wider hover:text-gray-300 transition-colors"
          @click="toggleMenu"
        >
          {{ item }}
        </a>
      </nav>
    </div>
  </section>
</template>

<style>
</style>
