<script setup>
import { ref } from 'vue'

defineProps({
  isDark: Boolean,
})

const email = ref('')
const showError = ref(false)

function handleSubmit() {
  const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/
  if (!emailRegex.test(email.value)) {
    showError.value = true
    return
  }
  showError.value = false
  alert(`Thanks! We'll be in touch at ${email.value}`)
  email.value = ''
}
</script>
<template>
  <section
    id="early-access"
    class="py-16 px-6 transition-colors duration-500"
    :class="isDark ? 'bg-dark-footer' : 'bg-light-section'"
  >
    <div
      class="max-w-2xl mx-auto rounded-xl p-10 md:p-12 text-center shadow-xl"
      :class="isDark ? 'bg-dark-intro' : 'bg-white'"
    >
      <h2
        class="text-2xl md:text-3xl font-bold font-raleway mb-4"
        :class="isDark ? 'text-white' : 'text-gray-800'"
      >
        Get early access today
      </h2>
      <p
        class="text-sm md:text-base leading-relaxed mb-8"
        :class="isDark ? 'text-gray-300' : 'text-gray-600'"
      >
        It only takes a minute to sign up and our free starter tier is extremely
        generous. If you have any questions, our support team would be happy to help you.
      </p>

      <!-- Email form -->
      <form
        @submit.prevent="handleSubmit"
        class="flex flex-col sm:flex-row gap-4"
        novalidate
      >
        <div class="flex-1">
          <label for="email" class="sr-only">Email address</label>
          <input
            id="email"
            v-model="email"
            type="email"
            placeholder="email@example.com"
            required
            class="input-field w-full border"
            :class="
              isDark
                ? 'bg-dark-main text-white border-gray-600 placeholder-gray-500'
                : 'bg-white text-gray-800 border-gray-300 placeholder-gray-400'
            "
            aria-describedby="email-error"
          />
          <p
            v-if="showError"
            id="email-error"
            class="mt-1 text-xs text-red-400 text-left pl-4"
            role="alert"
          >
            Please enter a valid email address.
          </p>
        </div>

        <button type="submit" class="btn-primary whitespace-nowrap">
          Get Started For Free
        </button>
      </form>
    </div>
  </section>
</template>
<style scoped></style>