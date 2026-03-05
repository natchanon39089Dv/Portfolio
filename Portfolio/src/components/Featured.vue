
<script setup>
const featured = {
  title: "Featured Project: Student Registration",
  desc: "Vue app with list, toggle detail, and registration actions. Clean components and state handling.",
  tech: ["Vue 3", "Bootstrap", "JSON Server"],
  demo: "#",
  code: "#"
}
</script>

<template>
  <section class="container container-narrow pb-5" id="featured">
    <div class="card-clean p-4 p-md-5">
      <div class="d-flex justify-content-between flex-wrap gap-2 align-items-start">
        <div>
          <h2 class="section-title mb-1">{{ featured.title }}</h2>
          <p class="small-muted mb-3">{{ featured.desc }}</p>

          <div class="d-flex flex-wrap gap-2 mb-3">
            <span class="badge badge-soft rounded-pill" v-for="t in featured.tech" :key="t">{{ t }}</span>
          </div>

          <div class="d-flex flex-wrap gap-2">
            <a class="btn btn-dark btn-clean" :href="featured.demo" target="_blank">Live Demo</a>
            <a class="btn btn-outline-dark btn-clean" :href="featured.code" target="_blank">Source Code</a>
          </div>
        </div>

        <div class="text-end">
          <div class="badge badge-soft rounded-pill px-3 py-2">
            <i class="bi bi-stars me-1"></i> Bestseller
          </div>
        </div>
      </div>
    </div>
  </section>
</template>