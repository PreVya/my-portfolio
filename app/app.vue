<template>
  <div class="scroll-smooth antialiased text-slate-100 bg-slate-900">
    <Navbar />

    <main class="pt-24">
      <Hero />
      <About />
      <Projects />
      <Skills />
      <Contact />
    </main>

    <footer class="py-8 text-center text-sm text-slate-400">
      <div class="max-w-5xl mx-auto px-6">© Prerana Vayavahare — Built with Nuxt & Tailwind #VibeCoded</div>
    </footer>
  </div>
</template>

<script setup>
import '../assets/css/tailwind.css'
import Navbar from '../components/Navbar.vue'
import Hero from '../components/Hero.vue'
import About from '../components/About.vue'
import Projects from '../components/Projects.vue'
import Skills from '../components/Skills.vue'
import Contact from '../components/Contact.vue'
</script>
