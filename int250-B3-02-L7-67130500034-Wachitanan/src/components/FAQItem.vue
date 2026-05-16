<script setup>
import { ref } from 'vue'

defineProps({
  question: String,
  answer: String,
  isDark: Boolean,
})

const isOpen = ref(false)
function toggle() {
  isOpen.value = !isOpen.value
}

</script>
<template>
  <div
    class="faq-item"
    :class="isDark ? 'border-gray-600' : 'border-gray-300'"
  >
    <button
      class="faq-question w-full text-left"
      :class="isDark ? 'text-white' : 'text-gray-800'"
      :aria-expanded="isOpen"
      @click="toggle"
      @keydown.enter="toggle"
      @keydown.space.prevent="toggle"
    >
      <span class="text-sm md:text-base pr-4">{{ question }}</span>
      
      <svg
        xmlns="http://www.w3.org/2000/svg"
        class="w-5 h-5 flex-shrink-0 transition-transform duration-300 text-cyan-fylo"
        :class="isOpen ? 'rotate-180' : ''"
        fill="none"
        viewBox="0 0 24 24"
        stroke="currentColor"
        aria-hidden="true"
      >
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
      </svg>
    </button>

    <Transition name="faq">
      <div
        v-show="isOpen"
        class="mt-4 text-sm leading-relaxed"
        :class="isDark ? 'text-gray-300' : 'text-gray-600'"
      >
        {{ answer }}
      </div>
    </Transition>
  </div>
</template>
<style scoped>
.faq-enter-active,
.faq-leave-active {
  transition: all 0.3s ease;
}
.faq-enter-from,
.faq-leave-to {
  opacity: 0;
  transform: translateY(-8px);
}
</style>