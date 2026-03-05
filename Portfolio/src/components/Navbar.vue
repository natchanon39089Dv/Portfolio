<script setup>
const links = [
  { id: "home", label: "Home" },
  { id: "featured", label: "Featured" },
  { id: "about", label: "About" },
  { id: "projects", label: "Projects" },
  { id: "contact", label: "Contact" }
]
</script>

<template>
  <nav class="navbar navbar-expand-lg sticky-top nav-clean">
    <div class="container container-narrow py-2">
      <a class="navbar-brand fw-bold" href="#home">
        RMx<span class="small-muted">.portfolio</span>
      </a>

      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#nav">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div id="nav" class="collapse navbar-collapse">
        <ul class="navbar-nav ms-auto align-items-lg-center gap-lg-2">
          <li class="nav-item" v-for="l in links" :key="l.id">
            <a class="nav-link" :href="`#${l.id}`">{{ l.label }}</a>
          </li>
          <li class="nav-item ms-lg-2">
            <a class="btn btn-dark btn-clean px-3" href="#contact">
              <i class="bi bi-envelope me-1"></i> Contact
            </a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>