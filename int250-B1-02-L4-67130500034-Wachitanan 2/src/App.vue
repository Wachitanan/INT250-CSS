<script setup>
import ProfileCard from './components/ProfileCard.vue';

</script>

<template>
  
    <div class="flex items-center justify-center gap-8 min-h-screen bg-gradient-to-br from-green-500 to-sky-400">
    <ProfileCard
    background1="../profile/bg_wachitanan.jpg"
     profileimg1="../profile/wachitanan.jpg"
     name1="Wachitanan Supho"
     subheading1="Student, 20, KMUTT"
     followers1="331"
     following1="312"

     background2="../profile/bg_natthasith.jpg"
     profileimg2="../profile/natthasith.jpg"
     name2="Natthasith Boonheng"
     subheading2="Student, 20, KMUTT"
     followers2="497"
     following2="640"

     background3="../profile/bg_jackkapong.jpg"
     profileimg3="../profile/jackkapong.jpg"
     name3="Jackkapong Karapinvong"
     subheading3="Student, 20, KMUTT"
     followers3="795"
     following3="874">
    </ProfileCard>
    </div>
    
</template>

<style scoped></style>
