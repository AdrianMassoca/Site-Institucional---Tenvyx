<script setup>
import { ArrowDown, ArrowUpRight, Activity, ShieldCheck, Workflow } from 'lucide-vue-next'
</script>

<template>
  <section id="inicio" class="hero-section">
    <div class="hero-bg-image"></div>
    <div class="hero-grid-lines"></div>
    <div class="hero-orb orb-one"></div><div class="hero-orb orb-two"></div>
    <div class="container hero-layout">
      <div class="hero-copy" data-reveal>
        <div class="eyebrow"><span class="status-dot"></span> TECNOLOGIA COM INTELIGÊNCIA</div>
        <h1>Transformamos complexidade em <span class="gradient-text">evolução digital.</span></h1>
        <p class="hero-description">Desenvolvemos soluções digitais que conectam tecnologia, processos e pessoas para tornar operações mais inteligentes.</p>
        <div class="hero-actions">
          <a class="button button-primary" href="#contato">Iniciar um projeto <ArrowUpRight :size="18" /></a>
          <a class="button button-ghost" href="#solucoes">Explorar soluções <ArrowDown :size="17" /></a>
        </div>
        <div class="hero-proof">
          <span class="proof-line"></span>
          <span>Estratégia <b>·</b> Engenharia <b>·</b> Resultado</span>
        </div>
      </div>

      <div class="hero-visual" data-reveal>
        <div class="visual-glow"></div>
        <div class="orbit orbit-a"></div><div class="orbit orbit-b"></div>
        <div class="visual-core">
          <img src="/images/logo-tenvyx.png" alt="Símbolo da TENVYX" />
          <span>TENVYX</span>
          <small>OPERATIONAL INTELLIGENCE</small>
        </div>
        <div class="float-card float-card-top">
          <span class="float-icon"><Activity :size="17" /></span>
          <span><b>Visão integrada</b><small>Dados conectados</small></span>
          <i class="live-indicator"></i>
        </div>
        <div class="float-card float-card-bottom">
          <span class="float-icon cyan"><Workflow :size="17" /></span>
          <span><b>Processos inteligentes</b><small>Fluxos mais claros</small></span>
        </div>
        <div class="visual-caption"><ShieldCheck :size="14" /> Tecnologia pensada para operações reais</div>
      </div>
    </div>
    <a class="scroll-cue" href="#solucoes"><span></span> ROLE PARA EXPLORAR</a>
  </section>
</template>
