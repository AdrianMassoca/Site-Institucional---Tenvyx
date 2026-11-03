<script setup>
import { Search, DraftingCompass, CodeXml, FlaskConical, Rocket } from 'lucide-vue-next'
import SectionHeading from './SectionHeading.vue'
const steps = [
  { n: '01', title: 'Descoberta', text: 'Entendemos o cenário, os objetivos e os desafios da operação.', icon: Search },
  { n: '02', title: 'Planejamento', text: 'Definimos escopo, prioridades, arquitetura e etapas de evolução.', icon: DraftingCompass },
  { n: '03', title: 'Desenvolvimento', text: 'Construímos a solução em ciclos organizados e acompanháveis.', icon: CodeXml },
  { n: '04', title: 'Validação', text: 'Testamos fluxos e refinamos a experiência antes da entrega.', icon: FlaskConical },
  { n: '05', title: 'Evolução', text: 'Preparamos a base para melhorias e novas necessidades.', icon: Rocket }
]
</script>

<template>
  <section class="section process-section">
    <div class="container">
      <SectionHeading eyebrow="NOSSO PROCESSO" title="Da estratégia à evolução, com método." description="Um caminho estruturado para transformar necessidades em soluções digitais consistentes." centered />
      <div class="process-track">
        <article v-for="step in steps" :key="step.n" class="process-step" data-reveal>
          <div class="process-icon"><component :is="step.icon" :size="21" /></div>
          <span class="process-number">{{ step.n }}</span>
          <h3>{{ step.title }}</h3>
          <p>{{ step.text }}</p>
        </article>
      </div>
    </div>
  </section>
</template>
