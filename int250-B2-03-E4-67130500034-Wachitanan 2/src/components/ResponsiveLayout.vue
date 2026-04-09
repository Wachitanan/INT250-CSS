<script setup>

</script>

<template>
    <div class="max-w-6xl mx-auto px-6 w-full bg-white border-2 border-slate-200 rounded-2xl p-5 mt-10">
        <h2 class="text-2xl font-bold ">6. Responsive Layout Example</h2>
        <p class="text-slate-500 text-sm mt-2">A reusable section layout with content on the left and summary panel on the right.</p>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-5">
            <div class="md:col-span-2 border border-gray-100 rounded-xl p-6 bg-slate-50">
                <h3 class="text-base font-bold text-gray-700 mb-3">Main Content Area</h3>
                <p class="text-sm text-gray-500 leading-relaxed">This area can be used for dashboard content, a feature section, course details, or product descriptions.
                    It demonstrates a simple reusable container pattern with consistent padding, rounded corners, and spacing.
                </p>
            </div>
        <div class="bg-blue-600 rounded-xl p-6 text-white">
            <h3 class="text-base font-bold mb-3">Summary Panel</h3>
            <p class="text-sm text-blue-100 leading-relaxed mb-6">
            This panel can be reused for quick stats, announcements, or call-to-action content.
            </p>
            <button class="px-5 py-2 bg-white text-blue-600 text-sm font-semibold rounded-lg hover:bg-blue-50 transition-colors duration-150">
            Learn More
            </button>
        </div>
        </div>
    </div>
</template>

<style scoped>
</style>