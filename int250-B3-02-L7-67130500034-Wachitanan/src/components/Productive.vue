<script setup>
defineProps({
  isDark: Boolean,
})
</script>

<template>
  <section
    class="py-16 md:py-24 px-6 transition-colors duration-500"
    :class="isDark ? 'bg-dark-main' : 'bg-white'"
  >
    <div class="max-w-5xl mx-auto flex flex-col md:flex-row items-center gap-10 md:gap-16">
      
      <div class="w-full md:w-1/2 flex-shrink-0">
        <img
          src="../images-fylo/illustration-stay-productive.png"
          alt="Person staying productive with Fylo"
          class="w-full max-w-sm mx-auto md:max-w-full"
        />
      </div>

      
      <div class="w-full md:w-1/2">
        <h2
          class="text-2xl md:text-3xl lg:text-4xl font-bold font-raleway mb-6 leading-tight"
          :class="isDark ? 'text-white' : 'text-gray-800'"
        >
          Stay productive,<br />wherever you are
        </h2>

        <p
          class="text-sm md:text-base leading-relaxed mb-4"
          :class="isDark ? 'text-gray-300' : 'text-gray-600'"
        >
          Never let location be an issue when accessing your files. Fylo has
          you covered for all of your file storage needs.
        </p>

        <p
          class="text-sm md:text-base leading-relaxed mb-6"
          :class="isDark ? 'text-gray-300' : 'text-gray-600'"
        >
          Securely share files and folders with friends, family and colleagues
          for live collaboration. No email attachments required.
        </p>

        
        <a
          href="#"
          class="inline-flex items-center gap-2 text-sm text-cyan-fylo border-b border-cyan-fylo pb-1 hover:opacity-70 transition-opacity duration-300"
          aria-label="See how Fylo works"
        >
          See how Fylo works
          <img
            src="../images-fylo/icon-arrow.svg"
            alt=""
            aria-hidden="true"
            class="w-4 h-4"
          />
        </a>
      </div>
    </div>
  </section>
</template>

<style scoped></style>