
<script setup>
import { MoveUp } from 'lucide-vue-next'

const year = new Date().getFullYear()
</script>

<template>
  <footer class="site-footer">
    <div class="container">

      <div class="footer-main">

        <a
          class="brand footer-brand"
          href="#inicio"
          aria-label="TENVYX - voltar ao início"
        >
          <img src="/images/logo-tenvyx.png" alt="" />

          <span class="brand-copy">
            <strong>TENVYX</strong>
            <small>INTELIGÊNCIA OPERACIONAL</small>
          </span>
        </a>

        <p>
          Tecnologia, estratégia e desenvolvimento para construir
          operações mais inteligentes e conectadas.
        </p>

        <a
          href="#inicio"
          class="back-top"
          aria-label="Voltar ao início da página"
        >
          Voltar ao topo
          <MoveUp :size="16" />
        </a>

      </div>

      <div class="footer-bottom">
        <span>
          © {{ year }} TENVYX. Todos os direitos reservados.
        </span>

        <span>
          TECH & DEVELOPMENT
          <b>·</b>
          BRASIL
        </span>
      </div>

    </div>
  </footer>
</template>
