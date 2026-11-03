<script setup>
import { onMounted } from 'vue'
import SiteHeader from './components/SiteHeader.vue'
import HeroSection from './components/HeroSection.vue'
import ServicesSection from './components/ServicesSection.vue'
import TechnologySection from './components/TechnologySection.vue'
import ProcessSection from './components/ProcessSection.vue'
import AboutSection from './components/AboutSection.vue'
import ContactSection from './components/ContactSection.vue'
import SiteFooter from './components/SiteFooter.vue'
import { useReveal } from './composables/useReveal'

useReveal()

onMounted(() => {
  document.documentElement.classList.add('app-ready')
})
</script>

<template>
  <SiteHeader />
  <main>
    <HeroSection />
    <div class="signal-strip" aria-label="Áreas de atuação">
      <div class="signal-track">
        <span>SOFTWARE SOB MEDIDA</span><i></i><span>INTELIGÊNCIA OPERACIONAL</span><i></i><span>APLICAÇÕES WEB</span><i></i><span>INTEGRAÇÃO DE SISTEMAS</span><i></i>
        <span>SOFTWARE SOB MEDIDA</span><i></i><span>INTELIGÊNCIA OPERACIONAL</span><i></i><span>APLICAÇÕES WEB</span><i></i><span>INTEGRAÇÃO DE SISTEMAS</span><i></i>
      </div>
    </div>
    <ServicesSection />
    <TechnologySection />
    <ProcessSection />
    <AboutSection />
    <ContactSection />
  </main>
  <SiteFooter />
</template>
