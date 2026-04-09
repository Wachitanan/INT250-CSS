<script setup>
const cards = [
  {
    badge: 'New',
    title: 'Basic Card',
    description: 'A simple reusable card for general content blocks in a dashboard or landing page.',
  },
  {
    badge: 'Profile',
    title: 'Student Profile Card',
    description: 'A profile summary card showing student status, program, and quick information.',
  },
  {
    badge: 'Event',
    title: 'Event Card',
    description: 'A reusable event component for workshops, seminars, or hackathon activities.',
  },
]
</script>

<template>
    <div class="max-w-6xl mx-auto px-6 w-full bg-white border-2 border-slate-200 rounded-2xl p-5 mt-10">
        <h2 class="text-2xl font-bold ">5. Cards</h2>
        <p class="text-slate-500 text-sm mt-2">Responsive card layout for reusable content blocks such as event, profile, or product cards.</p>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-5 mt-5">
            <div v-for="card in cards" :key="card.title" class="border border-gray-100 bg-slate-50 rounded-xl p-5 hover:shadow-md transition-shadow duration-200">
                <div class="flex justify-between items-center mb-3">
                    <span class="px-2.5 py-0.5 bg-blue-50 text-blue-500 text-xs font-semibold rounded-full">{{ card.badge }}</span>
                    <span class="text-xs text-gray-400">Reusable</span>
                </div>
                    <h3 class="text-base font-bold text-gray-800 mb-2">{{ card.title }}</h3>
                    <p class="text-sm text-gray-500 mb-5">{{ card.description }}</p>
                    <button class="px-4 py-1.5 border border-gray-200 text-gray-600 text-xs font-semibold rounded-lg hover:bg-gray-50 transition-colors duration-150">
                    View Details
                    </button>
            </div>

        </div>
    </div>

</template>

<style scoped>
</style>