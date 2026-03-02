<script setup>
</script>

<template>
    <div class="flex items-center justify-between px-16 py-10">
        <div class="flex items-center border-b border-gray-300 w-80 pb-1">
            <input 
            type="text" 
            placeholder="Search" 
            class="flex-1 text-gray-500 placeholder-gray-400 text-sm bg-transparent focus:outline-none">
            <svg class="w-4 h-4 text-gray-400" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                <circle cx="11" cy="11" r="7"/>
                <path d="M21 21l-4.35-4.35"/>
            </svg>
        </div>

        <button class="bg-black text-white text-sm px-8 py-3 rounded-full">Upload</button>
    </div>
</template>

<style scoped>
</style>