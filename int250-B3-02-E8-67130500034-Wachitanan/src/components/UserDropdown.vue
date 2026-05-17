<script setup>
import { ref } from 'vue'

const isOpen = ref(false)
</script>
<template>
    <div class="relative inline-block ">
        <!-- <button @click="toggleMenu">
        </button> -->
            <button
            @click="isOpen = !isOpen"
            class="hidden md:flex items-center gap-2 rounded-xl bg-white px-4 py-2 shadow-[0_0_15px_rgba(0,0,0,0.12)]">

                <div class="flex h-8 w-8 items-center justify-center rounded-full bg-blue-100 text-sm font-semibold text-[#6143f9]">
                    ST
                </div>
                    <span class="font-medium">
                        Student
                    </span>
            <svg xmlns="http://www.w3.org/2000/svg"
                class="h-4 w-4"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor">

                <path stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M19 9l-7 7-7-7" />
            </svg>
        </button>
        <div
            v-show="isOpen"
            class="absolute right-0 mt-2 w-48 rounded-2xl bg-white p-2 shadow-lg ring-1 ring-slate-200">

            <a href="#" class="block rounded-xl px-4 py-2 hover:bg-slate-100">
                Profile
            </a>

            <a href="#" class="block rounded-xl px-4 py-2 hover:bg-slate-100">
                Settings
            </a>

            <a href="#" class="block rounded-xl px-4 py-2 hover:bg-slate-100">
                Logout
            </a>

        </div>
    </div>
</template>

<style scoped></style>