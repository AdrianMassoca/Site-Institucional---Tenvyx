
<script setup>
import {
  ArrowUpRight,
  Code2,
  PanelsTopLeft,
  BrainCircuit,
  Network,
  Database,
  Gauge
} from 'lucide-vue-next'

import SectionHeading from './SectionHeading.vue'

const services = [
  {
    number: '01',
    title: 'Desenvolvimento web',
    text: 'Criamos plataformas digitais responsivas, intuitivas e escaláveis para fortalecer a presença digital e otimizar a experiência dos usuários.',
    icon: PanelsTopLeft,
    tag: 'Experiências digitais'
  },
  {
    number: '02',
    title: 'Sistemas personalizados',
    text: 'Desenvolvemos softwares alinhados às necessidades e regras de cada negócio, transformando processos específicos em soluções eficientes.',
    icon: Code2,
    tag: 'Software sob medida'
  },
  {
    number: '03',
    title: 'Inteligência operacional',
    text: 'Transformamos informações em indicadores estratégicos, proporcionando mais visibilidade, controle e segurança na tomada de decisões.',
    icon: BrainCircuit,
    tag: 'Decisões inteligentes'
  },
  {
    number: '04',
    title: 'Integrações e APIs',
    text: 'Conectamos plataformas, serviços e sistemas para facilitar a comunicação entre diferentes tecnologias e automatizar fluxos de informação.',
    icon: Network,
    tag: 'Conectividade inteligente'
  },
  {
    number: '05',
    title: 'Gestão e arquitetura de dados',
    text: 'Estruturamos e organizamos dados para garantir uma base tecnológica consistente, confiável e preparada para crescer.',
    icon: Database,
    tag: 'Estrutura tecnológica'
  },
  {
    number: '06',
    title: 'Consultoria tecnológica',
    text: 'Orientamos decisões técnicas e estratégicas, identificando oportunidades e definindo caminhos para a evolução digital.',
    icon: Gauge,
    tag: 'Estratégia e inovação'
  }
]
</script>

<template>
  <section id="solucoes" class="section services-section">
    <div class="container">

      <SectionHeading
        eyebrow="NOSSAS ESPECIALIDADES"
        title="Soluções inteligentes para desafios reais."
        description="Unimos engenharia, estratégia e tecnologia para desenvolver soluções que simplificam operações, conectam informações e impulsionam resultados."
      />

      <div class="services-grid">
        <article
          v-for="service in services"
          :key="service.number"
          class="service-card"
          data-reveal
        >
          <div class="service-card-top">
            <span class="service-number">{{ service.number }}</span>

            <component
              :is="service.icon"
              :size="22"
              :stroke-width="1.6"
              aria-hidden="true"
            />
          </div>

          <div>
            <span class="service-tag">{{ service.tag }}</span>

            <h3>{{ service.title }}</h3>

            <p>{{ service.text }}</p>
          </div>

          <a
            href="#contato"
            :aria-label="`Solicitar informações sobre ${service.title}`"
            class="service-link"
          >
            <ArrowUpRight :size="19" />
          </a>

          <div class="card-sheen"></div>
        </article>
      </div>

    </div>
  </section>
</template>
