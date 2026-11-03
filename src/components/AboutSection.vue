<script setup>
import { ArrowUpRight, Crosshair, Lightbulb, ShieldCheck } from 'lucide-vue-next'
import SectionHeading from './SectionHeading.vue'
</script>

<template>
  <section id="empresa" class="section about-section">
    <div class="container about-layout">
      <div class="about-visual" data-reveal>
        <div class="about-image-frame">
          <img src="/images/fundo-tenvyx.png" alt="Identidade visual tecnológica da TENVYX" />
          <div class="about-image-overlay"></div>
          <div class="about-image-label"><span class="status-dot"></span> TENVYX / TECH & DEVELOPMENT</div>
        </div>
        <div class="about-orbit"></div>
      </div>
      <div class="about-copy">
        <SectionHeading eyebrow="A TENVYX" title="Tecnologia com propósito. Soluções com direção." description="A TENVYX é apresentada como uma iniciativa de tecnologia voltada ao desenvolvimento de software, sistemas e soluções digitais para apoiar a evolução das operações empresariais." />
        <div class="values-list">
          <div><span><Crosshair :size="18" /></span><p><b>Foco no contexto</b><small>Entender a necessidade antes de definir a tecnologia.</small></p></div>
          <div><span><Lightbulb :size="18" /></span><p><b>Construção inteligente</b><small>Desenvolver soluções alinhadas aos objetivos do projeto.</small></p></div>
          <div><span><ShieldCheck :size="18" /></span><p><b>Base para evoluir</b><small>Organizar a estrutura para facilitar manutenção e crescimento.</small></p></div>
        </div>
        <a class="text-link" href="#contato">Conheça possibilidades para sua empresa <ArrowUpRight :size="17" /></a>
      </div>
    </div>
  </section>
</template>
