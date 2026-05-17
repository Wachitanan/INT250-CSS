<script setup>
import { ref } from 'vue';
import UserDropdown from './UserDropdown.vue';

// สร้างสถานะสำหรับเปิด/ปิดเมนู
const isMenuOpen = ref(false);

// ฟังก์ชันสลับสถานะ
const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};
</script>
<template>
    <header class="sticky top-0 z-30 border-b border-slate-200 bg-white/90 backdrop-blur dark:border-slate-800 dark:bg-slate-900/90">
    <!-- Navigation -->
    <nav class="flex items-center justify-between px-6 py-4 md:px-6">
        <!-- Logo -->
         <a href="#" class="flex items-center gap-3">
            <div class="flex h-10 w-10 items-center justify-center rounded-2xl bg-indigo-600 text-sm font-bold text-white shadow-sm">LS</div>
            
            <div>
                <h1 class="text-lg font-bold leading-tight">LearnSpace</h1>
                <p class="text-xs text-slate-500 dark:text-slate-400">Student Dashboard</p>
            </div>
         </a>

         <!-- Desktop Menu -->
          <ul class="hidden items-center gap-8 text-sm font-medium text-slate-600 md:flex dark:text-slate-300">
            <li>
                <a href="#" class="transition hover:text-indigo-600">Dashboard</a>
              </li>
              <li>
                <a href="#" class="transition hover:text-indigo-600">Courses</a>

              </li>
              <li>
                <a href="#" class="transition hover:text-indigo-600">Assignment</a>

              </li>
              <li>
                <a href="#" class="transition hover:text-indigo-600">Progress</a>

              </li>
          </ul>

          <div class="flex items-center gap-4">
          <UserDropdown />
          <!-- Hambergur mobile -->
          <button @click="toggleMenu" id="menu-btn" class="text-2xl md:hidden text-slate-700 dark:text-white">
            <svg xmlns="http://www.w3.org/2000/svg" 
                fill="none" 
                viewBox="0 0 24 24" 
                stroke-width="2" 
                stroke="currentColor" 
                class="w-7 h-7">
                <path stroke-linecap="round" 
                    stroke-linejoin="round" 
                    d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
            </svg>
          </button>
          </div>

    </nav>
          <div v-show="isMenuOpen">
          <ul id="mobile-menu" class="flex-col gap-4 p-4 text-sm font-medium text-slate-600 bg-white md:hidden dark:bg-slate-900 dark:text-slate-300">
            <li>
              <a href="#" @click="isMenuOpen = false" class="block transition hover:text-indigo-600">Dashboard</a>
              <a href="#" @click="isMenuOpen = false" class="block transition hover:text-indigo-600">Courses</a>
              <a href="#" @click="isMenuOpen = false" class="block transition hover:text-indigo-600">Assignment</a>
              <a href="#" @click="isMenuOpen = false" class="block transition hover:text-indigo-600">Progress</a>
              
            </li>
          </ul>
          </div>
          <!-- Desktop Dropdown -->

           <!-- Mobile Menu Button -->
    
    </header>
</template>

<style scoped></style>