<script>

</script>

<template>
    <nav class="bg-white relative z-50">
        <div class="max-w-6xl mx-auto px-6 py-5 flex items-center justify-between">
            <a href="#" class="text-2xl font-bold text-gray-900 tracking-tight">Shortly</a>

            <div class="hidden lg:flex items-center gap-8">
                <a href="#" class="text-gray-500 font-bold text-sm hover:teat-gray-900 transition-colors">Features</a>
                <a href="#" class="text-gray-500 font-bold text-sm hover:teat-gray-900 transition-colors">Pricing</a>
                <a href="#" class="text-gray-500 font-bold text-sm hover:teat-gray-900 transition-colors">Resources</a>
            </div>

            <div class="hidden lg:flex items-center gap-4">
                <a href="#" class="text-gray-500 font-bold text-sm hover:text-gray-900 transition-colors">Login</a>
                <a href="#" class="btn-cyan px-6 py-2 text-sm">Sign Up</a>
            </div>

            <button id="hamuburger-btn" class="lg:hidden flex flex-col gap-1.5 p-2" onclick="toggleMenu()">
                <span id="ham-line1" class="block w-6 h-0.5 bg-gray-600 transition-all duration-300"></span>
                <span id="ham-line2" class="block w-6 h-0.5 bg-gray-600 transition-all duration-300"></span>
                <span id="ham-line3" class="block w-6 h-0.5 bg-gray-600 transition-all duration-300"></span>
            </button>
        </div>

        <div id="mobile-menu" class="lg:hidden absolute top-full left-0 right-0 bg-[#3b3054] text-white rounded-xl mx-4 p-8 z-50">
            <div class="flex flex-col items-center gap-4 border-b border-gray-500 pb-6 mb-6">
                <a href="#" class="font-bold text-sm hover:text-[#2acfcf]">Features</a>
                <a href="#" class="font-bold text-sm hover:text-[#2acfcf]">Pricing</a>
                <a href="#" class="font-bold text-sm hover:text-[#2acfcf]">Resources</a>
            </div>
            <div class="flex flex-col items-center gap-4">
                <a href="%" class="font-bold text-sm hover:text-[#2acfcf]">Login</a>
                <a href="#" class="btn-cyan w-full text-center py-3 text-sm">Sign Up</a>
            </div>
        </div>
    </nav>
</template>

<style scoped>
   #mobile-menu { display: none; }
    #mobile-menu.open { display: block; }

    /* Hero illustration overflow */
    .hero-img-wrap { overflow: visible; }
</style>