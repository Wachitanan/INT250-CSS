<script>

</script>

<template>
    <div class="max-w-6xl mx-auto px-6 w-full bg-white border-2 border-slate-200 rounded-2xl p-5 mt-10">
        <h2 class="text-2xl font-bold ">3. Alerts</h2>
        <p class="text-slate-500 text-sm mt-2">Reusable feedback messages for success, warning, and error states.</p>

        <div class="mt-5 flex flex-col gap-4">
            <div class="px-5 py-4 bg-green-50 border border-green-200 rounded-2xl">
                <p class="text-green-800 text-sm font-bold">Succes Alert</p>
                <p class="text-green-800 text-xs">Your profile has been updated successfully.</p>
            </div>
            <div class="px-5 py-4 bg-yellow-50 border border-yellow-200 rounded-2xl">
                <p class="text-yellow-800 text-sm font-bold">Warning Alert</p>
                <p class="text-yellow-800 text-xs">Please review the form before submitting.</p>
            </div>
            <div class="px-5 py-4 bg-red-50 border border-red-200 rounded-2xl">
                <p class="text-red-800 text-sm font-bold">Error Alert</p>
                <p class="text-red-800 text-xs">Something went wrong. Please try again later.</p>
            </div>
        </div>
    </div>
</template>

<style scoped>
</style>