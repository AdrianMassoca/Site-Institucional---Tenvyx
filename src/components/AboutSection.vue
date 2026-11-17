
<script setup>
import {
  ArrowUpRight,
  Crosshair,
  Lightbulb,
  ShieldCheck
} from 'lucide-vue-next'

import SectionHeading from './SectionHeading.vue'
</script>

<template>
  <section id="empresa" class="section about-section">
    <div class="container about-layout">

      <div class="about-visual" data-reveal>
        <div class="about-image-frame">
          <img
            src="/images/fundo-tenvyx.png"
            alt="Identidade visual tecnológica da TENVYX"
          />

          <div class="about-image-overlay"></div>

          <div class="about-image-label">
            <span class="status-dot"></span>
            TENVYX / TECH & DEVELOPMENT
          </div>
        </div>

        <div class="about-orbit"></div>
      </div>

      <div class="about-copy">
        <SectionHeading
          eyebrow="SOBRE A TENVYX"
          title="Tecnologia com propósito. Inovação com direção."
          description="A TENVYX atua no desenvolvimento de software, sistemas e soluções digitais, conectando tecnologia e estratégia para atender às necessidades de cada negócio. Nosso propósito é transformar desafios operacionais em oportunidades de evolução."
        />

        <div class="values-list">

          <div>
            <span>
              <Crosshair :size="18" />
            </span>

            <p>
              <b>Entendimento estratégico</b>
              <small>
                Compreender os desafios e objetivos antes de definir cada solução.
              </small>
            </p>
          </div>

          <div>
            <span>
              <Lightbulb :size="18" />
            </span>

            <p>
              <b>Inovação aplicada</b>
              <small>
                Utilizar tecnologia de forma inteligente, com foco em necessidades reais.
              </small>
            </p>
          </div>

          <div>
            <span>
              <ShieldCheck :size="18" />
            </span>

            <p>
              <b>Compromisso com a evolução</b>
              <small>
                Construir soluções organizadas, sustentáveis e preparadas para crescer.
              </small>
            </p>
          </div>

        </div>

        <a class="text-link" href="#contato">
          Vamos construir novas possibilidades
          <ArrowUpRight :size="17" />
        </a>
      </div>

    </div>
  </section>
</template>
