
<script setup>
import iconAccessAnywhere from '../images-fylo/icon-access-anywhere.svg'
import iconSecurity from '../images-fylo/icon-security.svg'
import iconCollaboration from '../images-fylo/icon-collaboration.svg'
import iconAnyFile from '../images-fylo/icon-any-file.svg'

defineProps({
  isDark: Boolean,
})

const features = [
  {
    icon: iconAccessAnywhere,
    alt: 'Access anywhere icon',
    title: 'Access your files from anywhere',
    description:
      'The ability to use a smartphone, tablet, or computer to access your account means your files follow you everywhere.',
  },
  {
    icon: iconSecurity,
    alt: 'Security icon',
    title: 'Security you can trust',
    description:
      '2-factor authentication and user-controlled encryption are just a couple of the security features we allow to help secure your files.',
  },
  {
    icon: iconCollaboration,
    alt: 'Real-time collaboration icon',
    title: 'Real-time collaboration',
    description:
      'Securely share files and folders with friends, family and colleagues for live collaboration. No email attachments required.',
  },
  {
    icon: iconAnyFile,
    alt: 'Any file icon',
    title: 'Any file, anywhere',
    description:
      'Upload any file type you want, regardless of size and access it from any device at any time.',
  },
]
</script>
<template>
  <section
    id="features"
    class="py-16 md:py-24 px-6 transition-colors duration-500"
    :class="isDark ? 'bg-dark-main' : 'bg-light-gray'"
  >
    <div class="max-w-4xl mx-auto grid grid-cols-1 sm:grid-cols-2 gap-10 md:gap-16">
      <div
        v-for="feature in features"
        :key="feature.title"
        class="feature-card"
      >
        <img
          :src="feature.icon"
          :alt="feature.alt"
          class="w-16 h-16 mb-6 object-contain"
        />
        <h3
          class="text-lg font-bold font-raleway mb-3"
          :class="isDark ? 'text-white' : 'text-gray-800'"
        >
          {{ feature.title }}
        </h3>
        <p
          class="text-sm leading-relaxed"
          :class="isDark ? 'text-gray-300' : 'text-gray-600'"
        >
          {{ feature.description }}
        </p>
      </div>
    </div>
  </section>
</template>

<style scoped></style>