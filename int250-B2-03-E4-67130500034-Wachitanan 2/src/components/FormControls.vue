<script setup>
import { reactive } from 'vue'
 
const form = reactive({
  fullName: '',
  email: '',
  role: '',
  message: '',
})
 
// function submitForm() {
//   console.log('Form submitted:', form)
// }
 
// function submitForm() {
//   console.log('Form submitted:', form)
// }
</script>

<template>
    <div class="max-w-6xl mx-auto px-6 w-full bg-white border-2 border-slate-200 rounded-2xl p-5 mt-10">
        <h2 class="text-2xl font-bold ">4. Form Controls</h2>
        <p class="text-slate-500 text-sm mt-2">Consistent form patterns with labels, helper text, and validation style.</p>
        
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6 mt-5">
            <div>
                <label class="block text-sm font-semibold text-gray-700 mb-2">Full Name</label>
                <input
                type="text"
                placeholder="Enter your full name"
                v-model="form.fullName"
                class="w-full border border-gray-200 rounded-lg px-4 py-2.5 text-sm text-gray-700 placeholder-gray-300 focus:outline-none focus:ring-2 focus:ring-blue-400 transition"
                />
                <p class="text-sm text-gray-400 mt-1.5">Use a clear and complete student name.</p>
            </div>
            <div>
                <label class="block text-sm font-semibold text-gray-700 mb-2">Email Address</label>
                <input type="email"
                placeholder="Enter your email" 
                v-model="form.email"
                class="w-full border border-gray-200 rounded-lg px-4 py-2.5 text-sm text-gray-700 placeholder-gray-300 focus:outline-none focus:ring-2 focus:ring-blue-400 transition"/>
                <p class="text-sm text-gray-400 mt-1.5">Example:student@mail.kmutt.ac.th</p>
            </div>
            <div class="mb-6 md:col-span-2">
                <label class="block text-sm font-semibold text-gray-700 mb-2">Role</label>
                <select
                    v-model="form.role"
                    class="w-full border border-gray-200 rounded-lg px-4 py-2.5 text-sm text-gray-500 focus:outline-none focus:ring-2 focus:ring-blue-400 transition appearance-none bg-white">
                    <option value="" disabled>Select your role</option>
                    <option value="student">Student</option>
                    <option value="instructor">Instructor</option>
                    <option value="admin">Admin</option>
                </select>
            </div>
            <div class="mb-6 md:col-span-2">
                <label class="block text-sm font-semibold text-gray-700 mb-2">Message</label>
                <textarea v-model="form.message" 
                placeholder="Write your message here"row="4" 
                class="w-full border border-gray-200 rounded-lg px-4 py-2.5 text-sm text-gray-700 placeholder-gray-300 focus:outline-none focus:ring-2 focus:ring-blue-400 transition resize-none"></textarea>
                <p class="text-xs text-red-500 mt-1.5">This is an example of validation/helper text styling.</p>
            </div>

      </div>
      
    </div>
</template>

<style scoped>

</style>