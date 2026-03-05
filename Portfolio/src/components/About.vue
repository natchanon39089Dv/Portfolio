<script setup>
const skills = [
  "Vue 3 / Vite",
  "Bootstrap / UI",
  "Fetch API / JSON Server",
  "SQL (JOIN, SELECT)",
  "Python (sklearn basics)"
]
</script>

<template>
  <section class="container container-narrow py-5" id="about">
    <div class="row g-3">
      <div class="col-md-6">
        <div class="card-clean p-4 h-100">
          <h2 class="section-title mb-2">Brand Story</h2>
          <p class="small-muted mb-0">
            I build clean web apps with a focus on structure, readability, and user experience.
            This portfolio is designed like an online store—projects are displayed as products.
          </p>
        </div>
      </div>

      <div class="col-md-6">
        <div class="card-clean p-4 h-100">
          <h2 class="section-title mb-2">Skills</h2>
          <ul class="mb-0">
            <li v-for="s in skills" :key="s" class="mb-1">{{ s }}</li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>