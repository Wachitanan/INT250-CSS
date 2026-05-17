<script setup>
import { ref } from 'vue'

const courses = ref([
  {
    id: 1,
    code: 'INT250',
    title: 'CSS Framework',
    description: 'Learn how to build responsive and interactive web applications using Vue.js and Tailwind CSS.',
    status: 'In Progress',
    progress: 72,
  },
  {
    id: 2,
    code: 'INT161',
    title: 'Object-Oriented Programming',
    description: 'Practice Java programming, object-oriented design, and software development principles.',
    status: 'In Progress',
    progress: 58,
  },
])
</script>

<template>
  <div class="mt-5 m-5">
    <div class="space-y-2">
      <h1 class="mt-2 text-3xl font-bold tracking-tight">My Courses</h1>
      <p class="text-slate-500">Review your course progress and assignment status.</p>
    </div>

    <div class="grid grid-cols-1 gap-4 mt-6 md:grid-cols-2">
      <div
        v-for="course in courses"
        :key="course.id"
        class="flex flex-col justify-between w-full bg-white rounded-2xl ring-1 ring-slate-200 p-5 gap-4"
      >
        <div class="flex justify-between items-center">
          <span class="inline-flex px-3 py-1 bg-indigo-100 rounded-2xl text-sm text-indigo-600 font-bold">
            {{ course.code }}
          </span>
          <span class="inline-flex px-3 py-1 bg-yellow-100 rounded-2xl text-sm text-yellow-600 font-bold">
            {{ course.status }}
          </span>
        </div>

        
        <div class="space-y-1">
          <h2 class="text-xl font-bold tracking-tight">{{ course.title }}</h2>
          <p class="text-slate-500 text-sm leading-relaxed">{{ course.description }}</p>
        </div>

        <div class="space-y-1">
          <div class="flex justify-between text-sm text-slate-500">
            <span>Progress</span>
            <span>{{ course.progress }}%</span>
          </div>
          <div class="w-full bg-slate-200 rounded-full h-2">
            <div
              class="bg-indigo-600 h-2 rounded-full transition-all duration-500"
              :style="{ width: course.progress + '%' }"
            ></div>
          </div>
        </div>

        <!-- Buttons -->
        <div class="flex gap-3 mt-1">
          <button
            class="bg-indigo-600 text-white font-semibold px-4 py-2 rounded-xl hover:bg-indigo-700 transition cursor-pointer"
          >
            View Course Details
          </button>
          <button
            class="border border-slate-300 text-slate-700 font-semibold px-4 py-2 rounded-xl hover:bg-slate-100 transition cursor-pointer"
          >
            Submit Assignment
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped></style>