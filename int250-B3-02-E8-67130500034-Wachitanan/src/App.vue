<script setup>
import AppNavbar from './components/AppNavbar.vue';
import CourseModal from './components/CourseModal.vue';
import StarCard from './components/StarCard.vue';
import CourseCard from './components/CourseCard.vue';
</script>

<template>
  <AppNavbar />
  <div class="md:m-4">
  <StarCard />
  <CourseModal />
  <CourseCard />
  </div>
</template>

<style scoped></style>
