<script>

</script>

<template>
    <footer class="py-12 px-6">
        <div class="max-2-6xl mx-auto">
            <div class="flex flex-col md:flex-row md:items-start gap-10 md:gap-16 text-center md:text-left">
                <div class="logo-text shrink-0 mb-2 md:mb-0 md:mr-8">Shortly</div>
                <div class="flex flex-col md:flex-row gap-8 flex-1 justify-center md:justify-start">
                    <div>
                        <h4>Features</h4>
                        <a href="#">Link Shortening</a>
                        <a href="#">Branded Links</a>
                        <a href="#">Analytics</a>
                    </div>
                    <div>
                        <h4>Resources</h4>
                        <a href="#">Blog</a>
                        <a href="#">Developers</a>
                        <a href="#">Support</a>
                    </div>
                    <div>
                        <h4>Company</h4>
                        <a href="#">About</a>
                        <a href="#">Out Team</a>
                        <a href="#">Careers</a>
                        <a href="#">Contact</a>
                    </div>
                </div>

                <div class="flex justify-center md:justify-end items-center gap-5 md:ml-auto shrink-0">
                    <a href="#">
                        <img src="../assets/icon-facebook.svg" alt="Facebook">
                    </a>
                    <a href="#">
                        <img src="../assets/icon-twitter.svg" alt="Twitter">
                    </a>
                    <a href="#">
                        <img src="../assets/icon-pinterest.svg" alt="Pinterest">
                    </a>
                    <a href="#">
                        <img src="../assets/icon-instagram.svg" alt="Instagram">
                    </a>
                </div>

            </div>
        </div>
    </footer>
</template>

<style scoped>
    footer { background-color: #0e172a; color: var(--gray-violet); }
    footer .logo-text { color: #3b3054; font-weight: 700; font-size: 1.5rem; }
    footer h4 { color: white; font-weight: 700; font-size: 0.875rem; margin-bottom: 1rem; }
    footer a { color:white; font-size: 0.875rem; transition: color 0.2s; display: block; margin-bottom: 8px; }
    footer a:hover { color: var(--cyan); }
    .social-icon { width: 24px; height: 24px; fill: white; transition: fill 0.2s; }
    .social-icon:hover { fill: var(--cyan); }
    
</style>