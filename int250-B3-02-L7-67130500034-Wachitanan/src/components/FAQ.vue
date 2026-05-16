
<script setup>
import FAQItem from './FAQItem.vue'

defineProps({
  isDark: Boolean,
})

const faqItems = [
  {
    question: 'What is Fylo?',
    answer:
      'Fylo is a cloud storage service that stores all your most important files in one secure location. Access them whenever you need, share and collaborate with friends, family, and co-workers.',
  },
  {
    question: 'How can I request a new feature?',
    answer:
      'We love hearing from our users! You can reach out to our support team through the contact form on our website, or you can join our community forum to discuss and upvote feature requests.',
  },
  {
    question: 'Is this a mobile app?',
    answer:
      'Yes! Fylo is available on both iOS and Android platforms. You can download the app from the App Store or Google Play Store. We also have a fully responsive web version that works great on any device.',
  },
  {
    question: 'What does Chromebook Owners mean?',
    answer:
      'Chromebook owners are users who access Fylo primarily through the Chrome OS platform. Fylo works seamlessly on Chromebooks via our web application, giving you full access to all features without needing to install any additional software.',
  },
]
</script>
<template>
  <section
    id="faq"
    class="py-16 md:py-24 px-6 transition-colors duration-500"
    :class="isDark ? 'bg-dark-main' : 'bg-white'"
  >
    <div class="max-w-2xl mx-auto">
      <h2
        class="section-title mb-4"
        :class="isDark ? 'text-white' : 'text-gray-800'"
      >
        Frequently Asked Questions
      </h2>
      <p
        class="text-center text-sm md:text-base mb-10"
        :class="isDark ? 'text-gray-300' : 'text-gray-600'"
      >
        Here are some of our FAQs. If you have any other questions you'd like answered please feel free to email us.
      </p>

      <FAQItem
        v-for="(item, index) in faqItems"
        :key="index"
        :question="item.question"
        :answer="item.answer"
        :isDark="isDark"
      />
    </div>
  </section>
</template>

<style scoped></style>