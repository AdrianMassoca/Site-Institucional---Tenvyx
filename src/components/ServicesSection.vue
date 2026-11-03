<script setup>
import { ArrowUpRight, Code2, PanelsTopLeft, BrainCircuit, Network, Database, Gauge } from 'lucide-vue-next'
import SectionHeading from './SectionHeading.vue'

const services = [
  { number: '01', title: 'Aplicações web', text: 'Plataformas digitais responsivas, funcionais e preparadas para acompanhar a evolução do negócio.', icon: PanelsTopLeft, tag: 'Experiências digitais' },
  { number: '02', title: 'Sistemas sob medida', text: 'Soluções desenvolvidas em torno das necessidades, regras e rotinas específicas de cada operação.', icon: Code2, tag: 'Software personalizado' },
  { number: '03', title: 'Inteligência operacional', text: 'Organização de informações e visualização de indicadores para apoiar decisões com mais clareza.', icon: BrainCircuit, tag: 'Gestão orientada a dados' },
  { number: '04', title: 'Integrações e APIs', text: 'Conexão entre sistemas, serviços e bases de dados para reduzir silos de informação.', icon: Network, tag: 'Ecossistema conectado' },
  { number: '05', title: 'Dados e estrutura', text: 'Modelagem e organização de dados como base para aplicações consistentes e evolutivas.', icon: Database, tag: 'Fundação tecnológica' },
  { number: '06', title: 'Consultoria tecnológica', text: 'Apoio na definição de arquitetura, prioridades técnicas e caminhos para evolução digital.', icon: Gauge, tag: 'Direcionamento técnico' }
]
</script>

<template>
  <section id="solucoes" class="section services-section">
    <div class="container">
      <SectionHeading eyebrow="O QUE FAZEMOS" title="Tecnologia que trabalha a favor do seu negócio." description="Da ideia à operação, criamos soluções digitais conectadas aos desafios reais de cada empresa." />
      <div class="services-grid">
        <article v-for="service in services" :key="service.number" class="service-card" data-reveal>
          <div class="service-card-top"><span class="service-number">{{ service.number }}</span><component :is="service.icon" :size="22" :stroke-width="1.6" /></div>
          <div><span class="service-tag">{{ service.tag }}</span><h3>{{ service.title }}</h3><p>{{ service.text }}</p></div>
          <a href="#contato" :aria-label="`Conversar sobre ${service.title}`" class="service-link"><ArrowUpRight :size="19" /></a>
          <div class="card-sheen"></div>
        </article>
      </div>
    </div>
  </section>
</template>
