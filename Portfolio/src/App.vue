<template>
  <Navbar />

  <main class="pt-4">
    <Hero />
    <Featured />
    <About />
    <Projects />
    <Contact />
    <Footer />
  </main>
</template>

<script setup>
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import Featured from './components/Featured.vue'
import About from './components/About.vue'
import Projects from './components/Projects.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'
</script>