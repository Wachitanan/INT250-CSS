<script setup>
defineProps([
    "profileimg1",
    "background1",
    "name1",
    "subheading1",
    "followers1",
    "following1",

    "profileimg2",
    "background2",
    "name2",
    "subheading2",
    "followers2",
    "following2",

    "profileimg3",
    "background3",
    "name3",
    "subheading3",
    "followers3",
    "following3",
]);
</script>

<template>
   <div class="flex gap-6 justify-center flex-wrap">

    <!-- Card -->
     <div class="bg-white shadow-lg rounded-2xl w-[280px] overflow-hidden text-center transition-transform duration-200 ease-out hover:scale-105 hover:shadow-xl flex-shrink-0">
        <!-- image header -->
         <div class="relative min-h-32 bg-cover bg-center" :style= "'background-image: url(' + background2 + ')'">

            <img src="../../profile/natthasith.jpg" alt="Prifile" class="inline-block w-32 h-32 rounded-full object-center object-cover border-6 border-white absolute top-full left- transform -translate-1/2 ">

         </div>

         <!-- Subheading -->
         <div class="px-6 pt-20 pb-6">
            <h2 class="font-bold text-gray-800 text-2xl mb-2 leading-snug line-clamp-2 min-h-[3.5em]">{{ name2 }}</h2>

            <h3 class="text-gray-600 text-lg">{{ subheading2 }}</h3>
         </div>

         <!-- Contact -->
          <a href="https://www.instagram.com/mix_nsth_/"  target="_blank">
            <div class="flex items-center gap-4 mx-2 mb-2 px-2 pt-3 pb-2 bg-white shadow-md rounded-2xl min-[100px] hover:shadow-lg transition">
               <div class="w-10 h-10 rounded-xl overflow-hidden flex-shrink-0">
                  <img src="../../profile/Instagram_icon.png.webp" alt="instagram" rel="noopener noreferrer" class="w-full h-full object-contain">
               </div>
               <span>Instagram</span>
            </div>
         </a>

         <a href="https://www.facebook.com/natthasith.boonheng.1/"  target="_blank">
            <div class="flex items-center gap-4 mx-2 mb-2 px-2 pt-3 pb-2 bg-white shadow-md rounded-2xl min-[100px] hover:shadow-lg transition">
               <div class="w-10 h-10 rounded-xl overflow-hidden flex-shrink-0">
                  <img src="../../profile/facebook.webp" alt="facebook" rel="noopener noreferrer" class="w-full h-full object-contain scale-200">
               </div>
               <span>Facebook</span>
            </div>
         </a>

            <a href="https://www.tiktok.com/@_mixyyy?_r=1&_t=ZS-93YYF6cc4SD"  target="_blank">
            <div class="flex items-center gap-4 mx-2 mb-2 px-2 pt-3 pb-2 bg-white shadow-md rounded-2xl hover:shadow-lg transition">
               <div class="w-10 h-10 rounded-xl overflow-hidden flex-shrink-0">
                  <img src="../../profile/tiktok.avif" alt="facebook" rel="noopener noreferrer" class="w-full h-full object-contain scale-200">
               </div>
               <span>Tiktok</span>
            </div>
         </a>

         <!-- Stats -->
         <div class="p-6 border-t border-gray-200 flex item-center justify-center gap-6">
            <!-- Followers -->
             <div>
               <h4 class="text-gray-600 text-sm">Followers</h4>
               <p class="font-bold text-gray-800 text-2xl">{{ followers2 }}</p>
             </div>

            <div>
               <h4 class="text-gray-600 text-sm">Following</h4>
               <p class="font-bold text-gray-800 text-2xl">{{ following2 }}</p>
            </div>

         </div>

    </div>
        <!-- Card 2 -->
     <div class="bg-white shadow-lg rounded-2xl w-[280px] overflow-hidden text-center transition-transform duration-200 ease-out hover:scale-105 hover:shadow-xl flex-shrink-0">
        <!-- image header -->
         <div class="relative min-h-32 bg-cover bg-center" :style= "'background-image: url(' + background1 + ')'">

            <img src="../../profile/wachitanan.jpg" alt="Prifile" class="inline-block w-32 h-32 rounded-full object-[50%_90%] overflow-hidden object-cover border-6 border-white absolute top-full left- transform -translate-1/2 ">

         </div>

         <!-- Subheading -->
         <div class="px-6 pt-20 pb-6">
            <h2 class="font-bold text-gray-800 text-2xl mb-2 leading-snug line-clamp-2 min-h-[3.5em]">{{ name1 }}</h2>

            <h3 class="text-gray-600 text-lg">{{ subheading1 }}</h3>
         </div>
                   
         <!-- Contact -->
         <a href="https://www.instagram.com/wachixii_/"  target="_blank">
            <div class="flex items-center gap-4 mx-2 mb-2 px-2 pt-3 pb-2 bg-white shadow-md rounded-2xl min-[100px] hover:shadow-lg transition">
               <div class="w-10 h-10 rounded-xl overflow-hidden flex-shrink-0">
                  <img src="../../profile/Instagram_icon.png.webp" alt="instagram" rel="noopener noreferrer" class="w-full h-full object-contain">
               </div>
               <span class="justify-center">Instagram</span>
            </div>
         </a>

         <a href="https://www.facebook.com/share/14T2MFxSmGN/?mibextid=wwXIfr"  target="_blank">
            <div class="flex items-center gap-4 mx-2 mb-2 px-2 pt-3 pb-2 bg-white shadow-md rounded-2xl min-[100px] hover:shadow-lg transition">
               <div class="w-10 h-10 rounded-xl overflow-hidden flex-shrink-0">
                  <img src="../../profile/facebook.webp" alt="facebook" rel="noopener noreferrer" class="w-full h-full object-contain scale-200">
               </div>
               <span>Facebook</span>
            </div>
         </a>

         <a href="https://www.tiktok.com/@waaaaaaaaachi?is_from_webapp=1&sender_device=pc"  target="_blank">
            <div class="flex items-center gap-4 mx-2 mb-2 px-2 pt-3 pb-2 bg-white shadow-md rounded-2xl hover:shadow-lg transition">
               <div class="w-10 h-10 rounded-xl overflow-hidden flex-shrink-0">
                  <img src="../../profile/tiktok.avif" alt="facebook" rel="noopener noreferrer" class="w-full h-full object-contain scale-200">
               </div>
               <span>Tiktok</span>
            </div>
         </a>

         <!-- Stats -->
         <div class="p-6 border-t border-gray-200 flex item-center justify-center gap-6">
            <!-- Followers -->
             <div>
               <h4 class="text-gray-600 text-sm">Followers</h4>
               <p class="font-bold text-gray-800 text-2xl">{{ followers1 }}</p>
             </div>

            <div>
               <h4 class="text-gray-600 text-sm">Following</h4>
               <p class="font-bold text-gray-800 text-2xl">{{ following1 }}</p>
            </div>

         </div>

    </div>
        <!-- Card 3 -->
     <div class="bg-white shadow-lg rounded-2xl w-[280px] overflow-hidden text-center transition-transform duration-200 ease-out hover:scale-105 hover:shadow-xl flex-shrink-0">
        <!-- image header -->
         <div class="relative min-h-32 bg-cover bg-center" :style= "'background-image: url(' + background3 + ')'">

            <img src="../../profile/jackkapong.jpg" alt="Prifile" class="inline-block w-32 h-32 rounded-full object-center object-cover border-6 border-white absolute top-full left- transform -translate-1/2">

         </div>

         <!-- Subheading -->
         <div class="px-6 pt-20 pb-6">
            <h2 class="font-bold text-gray-800 text-2xl mb-2 leading-snug line-clamp-2 min-h-[3.5em]">{{ name3 }}</h2>

            <h3 class="text-gray-600 text-lg">{{ subheading3 }}</h3>
         </div>

         <!-- Contact -->
         <a href="https://www.instagram.com/lucky_.05._/"  target="_blank">
            <div class="flex items-center gap-4 mx-2 mb-2 px-2 pt-3 pb-2 bg-white shadow-md rounded-2xl hover:shadow-lg transition">
               <div class="w-10 h-10 rounded-xl overflow-hidden flex-shrink-0">
                  <img src="../../profile/Instagram_icon.png.webp" alt="instagram" rel="noopener noreferrer" class="w-full h-full object-contain">
               </div>
               <span>Instagram</span>
            </div>
         </a>

         <a href="https://www.facebook.com/jackrapong.kornpinwong"  target="_blank">
            <div class="flex items-center gap-4 mx-2 mb-2 px-2 pt-3 pb-2 bg-white shadow-md rounded-2xl hover:shadow-lg transition">
               <div class="w-10 h-10 rounded-xl overflow-hidden flex-shrink-0">
                  <img src="../../profile/facebook.webp" alt="facebook" rel="noopener noreferrer" class="w-full h-full object-contain scale-200">
               </div>
               <span>Facebook</span>
            </div>
         </a>

         <a href="https://www.tiktok.com/@lucky.lk05"  target="_blank">
            <div class="flex items-center gap-4 mx-2 mb-2 px-2 pt-3 pb-2 bg-white shadow-md rounded-2xl hover:shadow-lg transition">
               <div class="w-10 h-10 rounded-xl overflow-hidden flex-shrink-0">
                  <img src="../../profile/tiktok.avif" alt="facebook" rel="noopener noreferrer" class="w-full h-full object-contain scale-200">
               </div>
               <span>Tiktok</span>
            </div>
         </a>

         <!-- Stats -->
         <div class="p-6 border-t border-gray-200 flex item-center justify-center gap-6">
            <!-- Followers -->
             <div>
               <h4 class="text-gray-600 text-sm">Followers</h4>
               <p class="font-bold text-gray-800 text-2xl">{{ followers3 }}</p>
             </div>

            <div>
               <h4 class="text-gray-600 text-sm">Following</h4>
               <p class="font-bold text-gray-800 text-2xl">{{ following3 }}</p>
            </div>

         </div>

    </div>
</div>
</template>

<style scoped></style>