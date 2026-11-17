
<script setup>
import {
  ArrowUpRight,
  Check,
  Boxes,
  ChartNoAxesCombined,
  MonitorSmartphone
} from 'lucide-vue-next'

import SectionHeading from './SectionHeading.vue'
</script>

<template>
  <section id="tecnologia" class="section technology-section">
    <div class="container technology-layout">

      <div class="technology-copy">
        <SectionHeading
          eyebrow="INTELIGÊNCIA OPERACIONAL"
          title="Conectamos informações. Ampliamos possibilidades."
          description="Desenvolvemos estruturas tecnológicas que aproximam processos, dados e pessoas, oferecendo uma visão mais clara e integrada de cada operação."
        />

        <ul class="check-list">
          <li>
            <Check :size="16" />
            Integração entre processos operacionais e gestão estratégica
          </li>

          <li>
            <Check :size="16" />
            Informações centralizadas e organizadas
          </li>

          <li>
            <Check :size="16" />
            Interfaces intuitivas para facilitar o acompanhamento
          </li>

          <li>
            <Check :size="16" />
            Estruturas preparadas para acompanhar a evolução do negócio
          </li>
        </ul>

        <a class="text-link" href="#contato">
          Descubra novas possibilidades
          <ArrowUpRight :size="17" />
        </a>
      </div>

      <div class="dashboard-scene" data-reveal>
        <div class="dashboard-glow"></div>

        <div class="dashboard-window">

          <div class="window-top">
            <div class="window-dots">
              <i></i>
              <i></i>
              <i></i>
            </div>

            <span>
              PAINEL OPERACIONAL
              <b>● DEMONSTRAÇÃO VISUAL</b>
            </span>

            <div class="window-menu">•••</div>
          </div>

          <div class="dashboard-content">

            <div class="dashboard-title">
              <div>
                <small>VISÃO GERAL</small>
                <h3>Central de operações</h3>
              </div>

              <span class="dashboard-period">
                Painel ilustrativo
              </span>
            </div>

            <div class="metric-row">

              <div class="metric-card">
                <span>Processos</span>
                <strong>Organizados</strong>
                <small class="metric-positive">
                  Fluxos conectados
                </small>
              </div>

              <div class="metric-card">
                <span>Informações</span>
                <strong>Integradas</strong>
                <small class="metric-blue">
                  Dados centralizados
                </small>
              </div>

            </div>

            <div class="chart-card">
              <div class="chart-head">
                <span>Fluxo de atividades</span>
                <small>ILUSTRAÇÃO</small>
              </div>

              <div class="chart-bars">
                <i
                  v-for="n in 18"
                  :key="n"
                  :style="{
                    height: `${22 + ((n * 37) % 68)}%`,
                    animationDelay: `${n * 35}ms`
                  }"
                ></i>
              </div>

              <div class="chart-labels">
                <span>ETAPA 01</span>
                <span>ETAPA 02</span>
                <span>ETAPA 03</span>
                <span>ETAPA 04</span>
              </div>
            </div>

            <div class="dashboard-bottom">
              <div>
                <Boxes :size="16" />
                Estrutura integrada
              </div>

              <div>
                <ChartNoAxesCombined :size="16" />
                Visão gerencial
              </div>

              <div>
                <MonitorSmartphone :size="16" />
                Desktop & Web
              </div>
            </div>

          </div>
        </div>

        <div class="dashboard-float">
          <span class="float-icon">
            <ChartNoAxesCombined :size="17" />
          </span>

          <span>
            <b>Visão unificada</b>
            <small>Operação + gestão</small>
          </span>
        </div>

      </div>
    </div>
  </section>
</template>
