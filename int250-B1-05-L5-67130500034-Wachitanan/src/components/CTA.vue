<script>

</script>

<template>
    <section class="cta-bg py-20 text-center">
        <h2 class="text-2xl md:text-3xl font-bold text-white mb-6">Boost your links today</h2>
        <a href="#shorten" class="btn-cyan inline-block px-10 py-3 text-base">Get Started</a>
  </section>

</template>

<style scoped>

    .cta-bg {
      background-color: #3b3054;
      background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='1440' height='250'%3E%3Cellipse cx='1300' cy='50' rx='400' ry='250' fill='%232acfcf' fill-opacity='0.15'/%3E%3Cellipse cx='100' cy='220' rx='300' ry='200' fill='%232acfcf' fill-opacity='0.10'/%3E%3C/svg%3E");
      background-size: cover;
    }

    .btn-cyan {
      background-color: #2acfcf;
      color: white;
      border-radius: 50px;
      font-weight: 700;
      transition: opacity 0.2s;
    }
    .btn-cyan:hover { opacity: 0.7; }

    .link-card { background: white; border-radius: 8px; }

    .copy-btn {
      background-color: var(--cyan);
      color: white;
      border-radius: 8px;
      font-size: 0.875rem;
      font-weight: 700;
      padding: 8px 24px;
      transition: opacity 0.2s;
      white-space: nowrap;
    }
    .copy-btn:hover { opacity: 0.7; }
    .copy-btn.copied {
      background-color: var(--dark-violet);
    }

    input.shorten-input {
      border-radius: 8px;
      padding: 14px 16px;
      font-size: 1rem;
      outline: none;
      border: 3px solid transparent;
    }
    input.shorten-input.error {
      border-color: var(--red);
    }
    input.shorten-input.error::placeholder { color: rgba(244,99,99,0.5); }
    .error-msg { color: var(--red); font-style: italic; font-size: 0.8rem; }

    /* Divider line in shorten section */
    .result-divider { height: 1px; background: #f0f0f0; margin: 0; }

</style>