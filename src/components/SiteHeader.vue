<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import { Menu, X, ArrowUpRight } from 'lucide-vue-next'

const menuOpen = ref(false)
const scrolled = ref(false)
const activeSection = ref('inicio')
const links = [
  { label: 'Início', href: '#inicio', id: 'inicio' },
  { label: 'Soluções', href: '#solucoes', id: 'solucoes' },
  { label: 'Tecnologia', href: '#tecnologia', id: 'tecnologia' },
  { label: 'Empresa', href: '#empresa', id: 'empresa' }
]
let observer

function updateScroll() {
  scrolled.value = window.scrollY > 24
}
function closeMenu() {
  menuOpen.value = false
}

onMounted(() => {
  updateScroll()
  window.addEventListener('scroll', updateScroll, { passive: true })
  observer = new IntersectionObserver((entries) => {
    entries.forEach((entry) => {
      if (entry.isIntersecting) activeSection.value = entry.target.id
    })
  }, { rootMargin: '-35% 0px -55% 0px' })
  links.forEach(({ id }) => {
    const section = document.getElementById(id)
    if (section) observer.observe(section)
  })
})
onUnmounted(() => {
  window.removeEventListener('scroll', updateScroll)
  observer?.disconnect()
})
</script>

<template>
  <header class="site-header" :class="{ 'is-scrolled': scrolled, 'menu-open': menuOpen }">
    <div class="container nav-shell">
      <a class="brand" href="#inicio" aria-label="TENVYX - início" @click="closeMenu">
        <img src="/images/logo-tenvyx.png" alt="" />
        <span class="brand-copy"><strong>TENVYX</strong><small>INTELIGÊNCIA OPERACIONAL</small></span>
      </a>

      <nav class="desktop-nav" aria-label="Navegação principal">
        <a v-for="link in links" :key="link.id" :href="link.href" :class="{ active: activeSection === link.id }">{{ link.label }}</a>
      </nav>

      <a class="nav-cta" href="#contato">Vamos conversar <ArrowUpRight :size="16" /></a>
      <button class="menu-toggle" type="button" :aria-label="menuOpen ? 'Fechar menu' : 'Abrir menu'" :aria-expanded="menuOpen" @click="menuOpen = !menuOpen">
        <X v-if="menuOpen" :size="22" /><Menu v-else :size="22" />
      </button>
    </div>

    <nav v-if="menuOpen" class="mobile-nav" aria-label="Menu mobile">
      <a v-for="link in links" :key="link.id" :href="link.href" @click="closeMenu">{{ link.label }}</a>
      <a href="#contato" class="mobile-nav-cta" @click="closeMenu">Vamos conversar <ArrowUpRight :size="16" /></a>
    </nav>
  </header>
</template>
