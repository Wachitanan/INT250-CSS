<script>

</script>

<template>
    <section id="shorten" class="bg-gray-100 py-16 relative -mt-2">
        <div class="max-w-4xl mx-auto px-6">
            <div class="shorten-bg rounded-xl p-6 md:p-10 relative overflow-hidden">
                <div id="shorten-form" class="flex flex-col md:flex-row gap-4 relative z-10">
                    <div class="flex-1 flex flex-col">
                        <input 
                        type="url"
                        placeholder="Shorter a link here..."
                        class="shorten-input w-full flex-1 bg-white text-gray-700 placeholder-gray-400 px-4 py-3 rounded-md"
                        />
                        <span id="error-msg" class="error-msg mt-1 hidden">Please add a link</span>
                    </div>
                    <button
                    type="button"
                    @click="shortenLink"
                    class="btn-cyan px-8 py-4 text-sm rounded-lg shrink-0 
                            hover:opacity-80 hover:scale-105 transition duration-200"
                    >
                    Shorten It!
                    </button>
                </div>
            </div>
            <div id="results-list" class="mt-6 flex flex-col gap-4"></div>
        </div>
        
    </section>
</template>

<style scoped>
   .shorten-bg {
      background-color: #3b3054;
      background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='800' height='200'%3E%3Cellipse cx='750' cy='50' rx='300' ry='200' fill='%232acfcf' fill-opacity='0.12'/%3E%3Cellipse cx='50' cy='180' rx='200' ry='150' fill='%232acfcf' fill-opacity='0.08'/%3E%3C/svg%3E");
      background-size: cover;
      background-position: center;

    }
    .btn-cyan {
        background-color: #2acfcf;
        color: white;
        font-weight: 400;
    }

</style>