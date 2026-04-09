<script setup>
import Buttons from './components/Buttons.vue';
import Badges from './components/Badges.vue';
import Alert from './components/Alert.vue';
import FormControls from './components/FormControls.vue';
import Cards from './components/Cards.vue';
import ResponsiveLayout from './components/ResponsiveLayout.vue';
import Navbar from './components/Navbar.vue';
</script>

<template>
  <div class="min-h-screen bg-slate-100">
    <Navbar />
    <Buttons />
    <Badges />
    <Alert />
    <FormControls />
    <Cards />
    <ResponsiveLayout />
  </div>
</template>

<style scoped></style>
