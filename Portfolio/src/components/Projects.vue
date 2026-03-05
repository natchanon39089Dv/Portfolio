<script setup>
const projects = [
  {
    title: "Student Registration",
    desc: "List students, toggle details, and register actions using components.",
    tags: ["Vue 3", "Bootstrap", "JSON Server"],
    demo: "#",
    code: "#"
  },
  {
    title: "Silver Price ML (Mini)",
    desc: "Regression/classification experiments with metrics and plots.",
    tags: ["Python", "sklearn", "matplotlib"],
    demo: "#",
    code: "#"
  },
  {
    title: "SQL JOIN Practice",
    desc: "JOIN, DISTINCT, BETWEEN exercises with clear outputs.",
    tags: ["SQL", "Database", "Query"],
    demo: "#",
    code: "#"
  }
]
</script>

<template>
  <section class="container container-narrow py-5" id="projects">
    <div class="d-flex justify-content-between align-items-end mb-3">
      <div>
        <h2 class="section-title mb-1">Products (Projects)</h2>
        <p class="small-muted mb-0">Each card is a project you can “buy” (view).</p>
      </div>
      <a class="text-decoration-none small-muted" href="#contact">Request demo →</a>
    </div>

    <div class="row g-3">
      <div class="col-md-4" v-for="p in projects" :key="p.title">
        <div class="card card-clean p-3 h-100">
          <div class="thumb"></div>

          <h5 class="fw-semibold mt-3 mb-1">{{ p.title }}</h5>
          <p class="small-muted mb-2">{{ p.desc }}</p>

          <div class="d-flex flex-wrap gap-2 mb-3">
            <span class="badge badge-soft rounded-pill" v-for="t in p.tags" :key="t">{{ t }}</span>
          </div>

          <div class="mt-auto d-flex gap-2">
            <a class="btn btn-dark btn-clean flex-fill" :href="p.demo" target="_blank">
              Live
            </a>
            <a class="btn btn-outline-dark btn-clean flex-fill" :href="p.code" target="_blank">
              Code
            </a>
          </div>
        </div>
      </div>
    </div>

    <div class="small small-muted mt-3">
      Replace “#” with your real links (GitHub, Netlify, etc.).
    </div>
  </section>
</template>