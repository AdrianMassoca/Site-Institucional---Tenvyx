<script setup>
import { ref } from 'vue'
import { ArrowUpRight, Mail, MessageSquareText, Send } from 'lucide-vue-next'
import SectionHeading from './SectionHeading.vue'

const form = ref({ name: '', email: '', company: '', message: '' })
const feedback = ref('')
const submitted = ref(false)

function submitForm() {
  submitted.value = true
  feedback.value = 'Os campos foram validados nesta demonstração. Para receber mensagens, conecte este formulário a um serviço de envio ou API.'
}
</script>

<template>
  <section id="contato" class="section contact-section">
    <div class="contact-aura"></div>
    <div class="container contact-layout">
      <div class="contact-copy">
        <SectionHeading eyebrow="VAMOS CONVERSAR" title="Sua próxima evolução começa com uma conversa." description="Conte um pouco sobre seu desafio. Vamos entender o cenário e explorar caminhos para transformar sua ideia em uma solução digital." />
        <div class="contact-detail"><span><Mail :size="18" /></span><div><b>Contato institucional</b><small>Utilize o formulário para apresentar seu projeto.</small></div></div>
        <div class="contact-detail"><span><MessageSquareText :size="18" /></span><div><b>Vamos entender sua necessidade</b><small>Compartilhe objetivos, contexto e expectativas.</small></div></div>
      </div>
      <form class="contact-form" @submit.prevent="submitForm">
        <div class="form-heading"><span>INICIAR UM PROJETO</span><small><i></i> FORMULÁRIO DEMONSTRATIVO</small></div>
        <label for="name">Nome</label>
        <input id="name" v-model.trim="form.name" autocomplete="name" placeholder="Como podemos chamar você?" required />
        <label for="email">E-mail</label>
        <input id="email" v-model.trim="form.email" type="email" autocomplete="email" placeholder="voce@empresa.com" required />
        <label for="company">Empresa <span>(opcional)</span></label>
        <input id="company" v-model.trim="form.company" autocomplete="organization" placeholder="Nome da sua empresa" />
        <label for="message">Como podemos ajudar?</label>
        <textarea id="message" v-model.trim="form.message" rows="4" placeholder="Descreva brevemente sua ideia ou desafio..." required></textarea>
        <button class="button button-primary form-submit" type="submit">Validar mensagem <Send :size="17" /></button>
        <p v-if="feedback" class="form-feedback" role="status">{{ feedback }}</p>
        <p v-else class="form-note">Demonstração visual: nenhum dado é enviado ou armazenado.</p>
      </form>
    </div>
  </section>
</template>
