<script>
export default {
  name: 'Creation',
  data() {
    return {
      creations: [
        {
          title: 'Deep Earth',
          desktop: '/src/assets/desktop/image-deep-earth.jpg',
          mobile: '/src/assets/mobile/image-deep-earth.jpg',
        },
        {
          title: 'Night Arcade',
          desktop: '/src/assets/desktop/image-night-arcade.jpg',
          mobile: '/src/assets/mobile/image-night-arcade.jpg',
        },
        {
          title: 'Soccer Team VR',
          desktop: '/src/assets/desktop/image-soccer-team.jpg',
          mobile: '/src/assets/mobile/image-soccer-team.jpg',
        },
        {
          title: 'The Grid',
          desktop: '/src/assets/desktop/image-grid.jpg',
          mobile: '/src/assets/mobile/image-grid.jpg',
        },
        {
          title: 'From Up Above VR',
          desktop: '/src/assets/desktop/image-from-above.jpg',
          mobile: '/src/assets/mobile/image-from-above.jpg',
        },
        {
          title: 'Pocket Borealis',
          desktop: '/src/assets/desktop/image-pocket-borealis.jpg',
          mobile: '/src/assets/mobile/image-pocket-borealis.jpg',
        },
        {
          title: 'The Curiosity',
          desktop: '/src/assets/desktop/image-curiosity.jpg',
          mobile: '/src/assets/mobile/image-curiosity.jpg',
        },
        {
          title: 'Make It Fisheye',
          desktop: '/src/assets/desktop/image-fisheye.jpg',
          mobile: '/src/assets/mobile/image-fisheye.jpg',
        },
      ],
    }
  },
}
</script>
<template>
  
  <section>
    <div class="@container max-w-6xl mx-auto my-32 px-6 text-gray-800 md:px-0">
      <div class="flex flex-col items-center mb-10 md:flex-row md:justify-between">
        <h2
          class="text-4xl text-center uppercase tracking-wider font-thin font-sans text-gray-800 md:text-left md:text-5xl">
          Our Creations
        </h2>

        <button
          class="hidden px-10 py-2 my-0 font-bold tracking-widest uppercase border-2 border-black hover:bg-black hover:text-white transition-colors duration-200 md:block">
          See All
        </button>
      </div>

      <div
        class="grid md:grid-cols-4 w-full gap-y-6  text-2xl text-white uppercase md:flex-row md:gap-y-8 md:gap-x-8">
        <div
          v-for="item in creations"
          :key="item.title"
          class="group relative overflow-hidden">
          
          <img
            :src="item.desktop"
            :alt="item.title"
            class="hidden w-full duration-200 md:block group-hover:scale-110 transition-transform"/>

          <img
            :src="item.mobile"
            :alt="item.title"
            class="w-full md:hidden"/>

          <div
            class="absolute top-0 bottom-0 right-0 left-0 bg-gradient-to-b from-transparent to-gray-800 group-hover:from-white/30 group-hover:to-gray-400/60 group-hover:opacity-80 transition-all duration-200">
          </div>
          <h5
            class="absolute px-6 md:px-10 w-52 bottom-4 md:bottom-8 transition-all duration-200 group-hover:scale-110 group-hover:text-black font-josefin font-light tracking-wider leading-tight">
            {{ item.title }}
          </h5>
        </div>
      </div>

      <div class="flex justify-center mt-10 md:hidden">
        <button
          class="w-full px-10 py-2 my-0 font-bold tracking-widest uppercase border-2 border-black hover:bg-black hover:text-white transition-colors duration-200 md:hidden">
          See All
        </button>
      </div>
    </div>
  </section>
</template>

<style>
</style>