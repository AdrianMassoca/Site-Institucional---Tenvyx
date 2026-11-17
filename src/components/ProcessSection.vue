
<script setup>
import {
  Search,
  DraftingCompass,
  CodeXml,
  FlaskConical,
  Rocket
} from 'lucide-vue-next'

import SectionHeading from './SectionHeading.vue'

const steps = [
  {
    n: '01',
    title: 'Descoberta',
    text: 'Analisamos o cenário, identificamos necessidades e compreendemos os objetivos estratégicos de cada negócio.',
    icon: Search
  },
  {
    n: '02',
    title: 'Planejamento',
    text: 'Estruturamos a solução, definimos prioridades, tecnologias e um caminho claro para o desenvolvimento.',
    icon: DraftingCompass
  },
  {
    n: '03',
    title: 'Desenvolvimento',
    text: 'Transformamos o planejamento em soluções digitais funcionais, utilizando práticas modernas de engenharia.',
    icon: CodeXml
  },
  {
    n: '04',
    title: 'Validação',
    text: 'Realizamos testes, avaliamos funcionalidades e refinamos cada detalhe para garantir uma entrega consistente.',
    icon: FlaskConical
  },
  {
    n: '05',
    title: 'Evolução',
    text: 'Acompanhamos novas necessidades e preparamos as soluções para melhorias e crescimento contínuo.',
    icon: Rocket
  }
]
</script>

<template>
  <section class="section process-section">
    <div class="container">

      <SectionHeading
        eyebrow="NOSSA METODOLOGIA"
        title="Cada etapa importa. Cada solução tem um propósito."
        description="Seguimos um processo estruturado que transforma desafios em soluções digitais, conectando estratégia, desenvolvimento e evolução."
        centered
      />

      <div class="process-track">
        <article
          v-for="step in steps"
          :key="step.n"
          class="process-step"
          data-reveal
        >
          <div class="process-icon">
            <component
              :is="step.icon"
              :size="21"
              :stroke-width="1.7"
            />
          </div>

          <span class="process-number">{{ step.n }}</span>

          <h3>{{ step.title }}</h3>

          <p>{{ step.text }}</p>
        </article>
      </div>

    </div>
  </section>
</template>
